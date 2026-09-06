# AI Infrastructure Learning Roadmap

这个仓库是我的 AI Infra / LLM Serving 学习总控中心：记录路线、当前交付物、工程卡点与每周复盘。

> 原则：以可运行项目驱动学习，而不是以课程进度驱动学习。

## 当前阶段

正在进行：**ThreadPool v0**

项目仓库：[cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool)

本周交付：实现一个支持多 worker、阻塞等待、`future` 和优雅关闭的 C++17 线程池。

## 项目路线

| 阶段 | 项目 | 主要能力 |
|---|---|---|
| 1–3 周 | [cpp-thread-pool](https://github.com/Zhihui-Cui/cpp-thread-pool) | C++17、并发基础、测试与 benchmark |
| 4–6 周 | concurrent-tcp-server | Socket、并发服务器、压测 |
| 7–10 周 | mini-transformer | Transformer 前向/训练基础 |
| 11–14 周 | cuda-kernels | CUDA / Triton 与性能分析 |
| 15–20 周 | mini-vllm | KV Cache、调度、Continuous Batching |
| 21 周后 | inference-service | Docker、监控、部署与 Agent |

## 使用方式

每天开始：只打开 [now.md](./now.md)，选中一个可验收任务。

每天结束：
1. 提交项目代码；
2. 记录真正解决的难点到 [blockers.md](./blockers.md)；
3. 更新本周任务状态。

每周日：在 [weekly-reviews](./weekly-reviews) 新建一份复盘。

## 仓库说明

- [roadmap.md](./roadmap.md)：未来 5–6 个月的大路线
- [now.md](./now.md)：本周唯一目标与每日任务
- [blockers.md](./blockers.md)：卡点、查阅方向与最终理解
- [resources.md](./resources.md)：真正用过、值得回看的资料
- [weekly-reviews](./weekly-reviews)：每周复盘记录
