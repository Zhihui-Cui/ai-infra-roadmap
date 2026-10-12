# AI Systems 学习总控

执行版本：2026-10-12，依据本人 2026-10-01 整合规划。W1 从 2026-09-06 起算，当前 W6（10/11–10/17）。

主线：独立训练 → 模型机制 → 可靠单卡评测 → 一个有证据的深入问题。个人时间线原文保留本地，此处只发布技术执行摘要。

## 现在做什么

先看 [本周任务](now.md)，再推进 [独立训练总任务 #1](https://github.com/Zhihui-Cui/ai-infra-roadmap/issues/1)。本周只交付一个能解释的最小训练，不等待 TCP 扩展。

## 仓库分工

| 仓库 | 用途 | 当前证据与安排 |
|---|---|---|
| [cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool) | C++ 并发基础 P0 | #8、#9 已关闭；已有有界队列和 Linux 串行基线记录。冻结功能，每周少量巩固 |
| [concurrent-tcp-server](https://github.com/Zhihui-Cui/concurrent-tcp-server) | 6–10h 请求路径练习 P1 | 已有单连接、单请求 echo；#1 尚开，补测及耗时记录未齐。不是已实现并发服务 |
| [llm-inference-lab](https://github.com/Zhihui-Cui/llm-inference-lab) | 持续主项目 P2 | 训练、Transformer、GPU 小实验、单卡推理评测与一个深度专题放同一仓库 |
| 本仓库 | 计划、状态、周复盘与跨项目入口 | 不放大模型权重，不堆放课程完整笔记 |

暂不新建 Mini-vLLM、CUDA 大全集、量化论文或 FPGA 项目。未来出现独立使用者、独立发布需求和稳定边界时再拆仓。

## 导航

- [阶段路线与门槛](roadmap.md)
- [主项目结构、周计划及验收](plans/llm-inference-lab.md)
- [TCP 限时练习](plans/concurrent-tcp-server.md)
- [每周复盘](weekly-reviews/README.md)
- [卡点](blockers.md)

## 状态如何判断

2026-10-12 核对了远程文件和 Issue，未在本次重新执行项目测试。已完成、指导下完成、尚未独立复做应分别记录。旧周报是历史快照，不覆盖最新证据；Issue 因延期关闭不等于完成。
