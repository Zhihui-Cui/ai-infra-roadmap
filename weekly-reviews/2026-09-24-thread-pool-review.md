# ThreadPool v0 检查与阶段推进（2026-09-24）

## 结论

按当前文档约定的学习项目 v0 范围，交付完成，可以进入 Concurrent TCP Server。项目交付与独立掌握程度分别记录；9 月 23 日复盘里的理解短板仍需巩固。

检查版本：[4f2279c140e643fafd24301afdc3f3837b26cad8](https://github.com/Zhihui-Cui/cpp-thread-pool/commit/4f2279c140e643fafd24301afdc3f3837b26cad8)。

## 实际核验

2026-09-24 从 GitHub 克隆独立副本，未修改实现。环境：Windows、MSYS2 UCRT64 GCC 16.2.0、CMake、Ninja。

- Debug 完整构建成功。
- CTest：task_queue_test、single_thread_executor_test、thread_pool_test，3/3 Passed，总计 0.88 秒，单测试超时 30 秒。
- Release 独立构建 thread_pool_benchmark 并运行，退出码 0；所有预热和正式轮次校验通过。
- GitHub Issue #1–#7 已勾选验收项，查询无开放 Issue。
- 阅读队列、线程池接口/实现、测试、benchmark、CMake 与 README。未进行穷尽并发验证或运行数据竞争检测器。

复验命令（需工具位于 PATH）：

~~~powershell
cmake -S . -B build-review -G Ninja -DCMAKE_BUILD_TYPE=Debug
cmake --build build-review
ctest --test-dir build-review --output-on-failure --timeout 30
cmake -S . -B build-review-release -G Ninja -DCMAKE_BUILD_TYPE=Release
cmake --build build-review-release --target thread_pool_benchmark
.\build-review-release\thread_pool_benchmark.exe
~~~

## 本次 benchmark 原始结果

每配置预热一次，正式五轮；1000 任务，每任务 100000 轮计算。

| worker | 五轮耗时（ms） | 中位数（ms） |
| --- | --- | --- |
| 1 | 139.203 / 137.049 / 137.362 / 154.498 / 154.182 | 139.203 |
| 2 | 67.564 / 68.391 / 66.662 / 67.137 / 66.992 | 67.137 |
| 4 | 34.178 / 33.772 / 34.461 / 33.518 / 33.713 | 33.772 |

checksum 均为 11208273736162531860。本次数据独立保留，不与 README 的历史轮次混合；不能据此给出通用最佳 worker 数量或推断性能变化原因。计时包含提交、执行和结果汇总，不包含建池/关池；没有直接串行耗时基线。

## 审查结论与已知边界

未发现阻止进入下一学习阶段的确定性缺陷；这不是生产级安全或无数据竞争保证。

- 入队和停止状态共享外层锁，worker 带谓词等待，取任务后解锁执行，退出时排空已接受任务。
- stop 仅支持单个外部调用线程；不支持并发 stop、worker 自身 stop/析构。README 已明确这些限制。
- 参数按值保存；不完整支持将 unique_ptr 等参数按值移动交给目标函数，文档已声明。
- assert 测试必须在 Debug 等未定义 NDEBUG 的配置下运行。
- 尚无 ThreadSanitizer 证据，也未模拟线程创建中途失败；属于后续验证项。
- 无界任务队列与阻塞任务是接入服务器时必须重新审视的点：慢客户端会占用 worker，单纯 pool.stop() 不能唤醒卡在 recv 的任务。

## 下一步

本周半天到一天巩固关键流程，W4 开始 Linux 阻塞 TCP echo，W5 复用线程池，W6 完成压测。延后公平调度、无锁队列等扩展。

保留 [9 月 23 日复盘](2026-09-23-thread-pool.md) 原有自评与实验想法；其中“待提交/关闭”的历史状态已由本次检查更新。
