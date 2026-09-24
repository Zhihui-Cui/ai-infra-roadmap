# AI Systems / MLSys 学习总控

目标：以 C++ / Linux / 系统能力为基础，逐步进入 LLM 推理系统，同时积累可复现的系统实验与研究能力。

## 当前进度（2026-09-24）

- **ThreadPool v0 已完成**：[cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool)，Issue #1–#7 均已关闭。
- 2026-09-24 独立复验：Debug 构建成功，CTest 3/3 通过；Release benchmark 校验通过。详见 [阶段检查](weekly-reviews/2026-09-24-thread-pool-review.md)。
- **当前：W3 收尾与网络项目准备；下一阶段：Concurrent TCP Server。**
- 先做半天到一天的独立巩固，再推进新项目；项目交付完成不等于所有知识已熟练。

## 项目地图

| 项目 | 状态 | 交付重点 |
| --- | --- | --- |
| [cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool) | v0 完成 | 多 worker、条件变量、future、优雅关闭、测试与性能实验 |
| concurrent-tcp-server | 待创建，下一项目 | Linux socket、并发连接、资源生命周期与压测 |
| mini-transformer | 后续 | 模型原理、训练/推理、正确性验证 |
| cuda-kernels | 后续 | CUDA/Triton、内存访问、profiling |
| mini-vllm | 后续 | KV Cache、调度、continuous batching、性能指标 |
| inference-service | 后续 | 服务化、可观测性、部署与分布式基础 |

后续项目到阶段再创建。新项目范围与候选任务见 [TCP Server 计划](plans/concurrent-tcp-server.md)。

## 日常使用

1. 开始前看 [now.md](now.md)，只选一个可验收任务。
2. 自己写第一版；AI 先给提示、审查和报错解释，按需请求参考实现。
3. 结束前运行相应测试、检查 diff、提交代码；记录有复用价值的卡点。
4. 每周复盘一次，按实际理解调整下一周。

## 索引

- [roadmap.md](roadmap.md)：分阶段路线与日期
- [now.md](now.md)：当前行动和下一周验收
- [blockers.md](blockers.md)：卡点记录
- [resources.md](resources.md)：实际用过的资料
- [weekly-reviews](weekly-reviews)：复盘与验证记录

周数以 2026-09-06（日）为 W1 起点，周日到周六；不使用 ISO 周号。
