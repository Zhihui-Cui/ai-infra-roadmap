# AI Systems 学习总控

以 C++ / Linux 系统能力为基础，推进模型正确性、单卡推理和性能实验。2026-09-24 起按个人时间线新版计划执行，替代此前立即进入三周 TCP 项目的安排。

## 项目与能力状态

| 项目 | 项目状态 | 能力状态 |
| --- | --- | --- |
| [cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool) | v0 已交付，原 #1–#7 已关闭 | 核心机制独立验收中 |
| concurrent-tcp-server | 待创建；W6–W7 两周练习 | 待学习 |
| llm-inference-lab（建议名） | W8 起的持续主项目，届时创建 | 训练循环 → 模型/KV → GPU → serving |

模型、算子和推理服务放入一个持续主项目，不再分别创建 mini-transformer、cuda-kernels、mini-vllm 等教程仓库。

## 当前入口

- [now.md](now.md)：当前唯一主任务。
- [路线与每周验收](roadmap.md)：W3–W26。
- [网络练习计划](plans/concurrent-tcp-server.md)：W6–W7。
- [线程池独立验收 #8](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/8)
- [Linux 与并发验证 #9](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/9)
- [串行基线与任务粒度 #10](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/10)

历史：[2026-09-24 独立构建检查](weekly-reviews/2026-09-24-thread-pool-review.md)。该报告测试证据保留，文末旧排期以当前 roadmap/now 为准。新增巩固任务不否定原 v0 交付。

## 使用规则

每周一个主要交付、最多三个子任务；先自己实现，卡住时要提示，完成后审查并延迟复做。区分实现完成、实测证据和独立能力。卡点写入 [blockers.md](blockers.md)，实际使用的资料写入 [resources.md](resources.md)，复盘写入 [weekly-reviews](weekly-reviews)。

W1 为 2026-09-06～09-12，按周日到周六计数。个人学校、实习意向和毕业材料信息保留本地文档，本仓库公开学习执行摘要。
