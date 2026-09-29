# 模型效率与 AI Systems 学习总控

更新：2026-09-29。当前暂定主攻模型推理优化、效率算法及相关系统工程，保留应用算法的选择权。重点是独立实现、可信实验与可说明的贡献；年底根据项目和外部反馈调整。

本页与 roadmap/now 按 9 月 29 日新规划执行，替代 9 月 23–24 日旧排期。个人职业比较与学校信息保留本地，不上传原文。

## 项目状态与能力状态

| 项目 | 交付状态 | 当前动作 |
| --- | --- | --- |
| [cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool) | v0 已完成；main 仍为 4f2279c | #8 已勾选四项，完成结果/异常接回并补证据；#9 Linux 构建调试 |
| [concurrent-tcp-server](https://github.com/Zhihui-Cui/concurrent-tcp-server) | 只有说明，无实现 | 缩为总计 6–10h，只执行 #1；#2–#4 暂不安排 |
| llm-inference-lab（建议名） | 主项目待启动，未在本次建立仓库 | 10 月中旬开始独立训练 → Transformer/KV → 效率实验 |

#8 的勾选为本人报告；独立练习尚未出现在远程 main，也无 Issue 评论证据，不视为本次实测通过。原 v0 的 9/24 构建证据继续保留。

## 任务入口

- [当前该做什么](now.md)
- [新路线与时间预算](roadmap.md)
- [线程池 #8：核心收尾](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/8)
- [线程池 #9：Linux 构建与调试](https://github.com/Zhihui-Cui/cpp-thread-pool/issues/9)
- [网络最小练习](plans/concurrent-tcp-server.md)
- [下一主任务：独立训练与验证](https://github.com/Zhihui-Cui/ai-infra-roadmap/issues/1)

## 管理原则

项目完成、运行证据和独立能力分别记录。每次只推进当前一个小步骤，AI 先给提示再审查；已完成任务不重做。
历史 [复盘](weekly-reviews) 保留当时语境，其中旧未来排期以现行 roadmap/now 为准。
