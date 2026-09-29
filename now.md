# 当前：接回最小线程池的结果与异常

2026-09-29，W4（9/27～10/3）。依据最新规划更新；不重新执行已经勾选的练习。

## 远程已看到的进度

[线程池 #8](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/8) 已勾选：时序图、三个小练习、最小池实现、提示与错误记录。这是本人记录的状态；main 仍为原 v0，尚未看到这些独立练习的代码或运行证据。

## 今天只做这一项

在你已写出的最小池中接回 packaged_task/future：

1. 先实现并运行返回 42 的任务。
2. 再覆盖 void、任务抛异常、异常经 get 取回、随后任务仍能执行。
3. 用自己的话解释 get 与 join 的区别；保存练习与测试命令/实际结果，提交后关联 #8。

不要求通用参数包或完美转发。先自己写，卡住时请求一个提示。原“3–7 天变体”转为后续可选复测，不阻塞 #8 关闭与进入模型阶段。测试未做就不勾选。

## 10 月上旬收尾

- 完成 [#9 Linux 构建和一次调试](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/9)。
- 原多生产者压力测试、竞态检测与 [#10 benchmark 补强](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/10) 留作后续可选，不继续扩张线程池。

## 随后

网络练习总计 6–10h，只完成 [最小请求路径](https://github.com/Zhihui-Cui/concurrent-tcp-server/issues/1)。原两周网络项目取消，不要求线程池接入、复杂并发或 p99 压测。

10 月中旬进入 [独立训练/验证/保存加载](https://github.com/Zhihui-Cui/ai-infra-roadmap/issues/1)，到 11 月上旬形成独立训练能力；无需等待扩展系统任务完成。

## 每周 30 小时

主项目12h、数学/ML6h、文献/实验设计4h、算法4h、C++/Linux2h、复盘/交流/投递准备2h。当前到 10 月上旬的线程池/Linux 收尾可占用主项目时间；进入模型阶段后系统巩固保持2h。训练基础未过时，部分文献时间改为训练实践。
