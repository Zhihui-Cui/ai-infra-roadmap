# 当前唯一目标：ThreadPool 核心机制独立验收

更新：2026-09-24，W3 剩余时间。依据个人时间线新版计划，替代之前“半天巩固后立即做 TCP”的排期。

## 状态

- 项目：v0 已交付，原 #1–#7 已完成。
- 验证：9/24 独立 Debug 构建和 CTest 3/3 通过，Release benchmark 校验通过。
- 能力：等待、任务包装、结果和关闭流程仍待独立验收。
- 当前任务：[Issue #8](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/8)。

## 本周三个子任务

- [ ] 不看源码画 submit 到 future 的时序，标注执行线程、对象所有权、锁范围。
- [ ] 独立写条件变量等待/唤醒小练习，解释等待谓词和关闭通知。
- [ ] 独立写延迟执行及 packaged_task/future 小练习，覆盖返回值、void 和异常。

允许查 API 文档；记录自己完成和需要提示的部分。今天先画时序，遇到不清楚的环节标问号，再用小练习验证。

## W4（9/27～10/3）

从空文件独立写只保存 std::function<void()> 的最小池，再接回结果与异常；建立 Linux 环境。原实现保留，练习使用独立目录。间隔 3–7 天复做一个变体。独立巩固约 15–25 小时，按实际进度调整。

## W5（10/4～10/10）

[Linux 与多生产者验证 #9](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/9)；
[串行基线与任务粒度 #10](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/10)。

## 之后

W6–W7（10/11～10/24）限时完成 Linux 并发任务服务；W8（10/25）进入 Python/PyTorch。详细验收见 [roadmap.md](roadmap.md)。

每周约 30 小时预算：实现/实验 14h、理论 6h、算法 4h、复盘 2h、缓冲/复测 4h。考试周缩小任务，不跳过前置验收。
