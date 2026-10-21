# AI Systems 学习总控

执行更新：2026-10-21。W1 从 2026-09-06 起算，当前 W7（10/18–10/24），按周日到周六统计。

主线：独立训练 → 模型机制 → 可靠单卡评测 → 一个有证据的深入问题。此处发布技术执行摘要，代码与实验输出放对应项目。

## 现在做什么

[本周任务](now.md) · [独立训练总任务 #1](https://github.com/Zhihui-Cui/ai-infra-roadmap/issues/1)。

已从 Python MSE 推进到 CPU 线性回归、MLP、DataLoader、训练/验证/测试、保存加载及早停。10/19 完整线性流程数值检查通过；其中包含 AI 审查与完整参考实现，**G1 独立训练验收尚未完成**。10/21 已补齐指导下两次故障闭环、标准化与二分类入门，当前优先配置/划分追溯及一次综合独立变体。

## 仓库分工

| 仓库 | 用途 | 当前证据与安排 |
|---|---|---|
| [cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool) | C++ 并发基础 P0 | 沿用已核对状态：#8、#9 已关闭；有界队列与 Linux 串行基线已记录。冻结功能，少量巩固 |
| [concurrent-tcp-server](https://github.com/Zhihui-Cui/concurrent-tcp-server) | 请求路径练习 P1 | 已有单连接、单请求 echo；10/12 本地读行七用例记录见旧快照。10/21 本人报告普通/分段复测完成；未附新日志，#1 不作全项通过 |
| [llm-inference-lab](https://github.com/Zhihui-Cui/llm-inference-lab) | 持续主项目 P2 | 新增标准化、广播排错、二分类与独立预测源码及五脚本核验；独立能力继续验收 |
| 本仓库 | 计划、状态、周复盘与跨项目入口 | 保存学习结论与下一步，链接实验原始证据 |

不新增 Mini-vLLM、CUDA 大全集、量化论文或 FPGA 项目。模型学习优先，系统扩展不足时续到巩固时段。

## 最新复盘

- [W7：截至 10/21 的跨项目进展](weekly-reviews/2026-10-21-W07-checkpoint.md)

- [W6：10/11–10/17 周总结](weekly-reviews/2026-10-17-W06.md)
- [W7：截至 10/19 的快照](weekly-reviews/2026-10-19-W07-checkpoint.md)
- [W6 截至 10/12 的历史快照](weekly-reviews/2026-10-12-W06-checkpoint.md)
- [W4](weekly-reviews/2026-10-03-W04.md) · [W5](weekly-reviews/2026-10-10-W05.md)

## 导航与证据口径

[使用说明](HOW_TO_USE.md) · [阶段路线与门槛](roadmap.md) · [主项目计划](plans/llm-inference-lab.md) · [TCP 限时练习](plans/concurrent-tcp-server.md) · [全部周报](weekly-reviews/README.md) · [卡点](blockers.md)。

本次核对远程记录、本人贴出的运行结果与本地源码，并在隔离副本核验代表性脚本。详细新日志只放主项目。成功运行、指导下完成与独立复做分别记账；未记录工时写未知；旧快照保留原貌，不倒填当时尚未完成的内容。
