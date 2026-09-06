# 路线图

目标：成为能够理解并实现 LLM 推理系统关键组件的工程师，并产出一条可验证的项目链。

## 阶段 1：C++ 并发基础（第 1–3 周）
- 项目：cpp-thread-pool
- 产出：线程安全队列、多 worker、条件变量、future、优雅关闭、测试与 benchmark。

## 阶段 2：并发网络服务（第 4–6 周）
- 项目：concurrent-tcp-server
- 产出：TCP 服务端、线程池集成、压测与性能分析。

## 阶段 3：模型基础（第 7–10 周）
- 项目：mini-transformer
- 产出：Transformer 核心组件、训练/推理流程说明。

## 阶段 4：GPU 性能（第 11–14 周）
- 项目：cuda-kernels
- 产出：CUDA/Triton 算子及性能对比。

## 阶段 5：推理引擎（第 15–20 周）
- 项目：mini-vllm
- 产出：KV Cache、调度器、Continuous Batching 与 benchmark。

## 原则
新知识只有在能帮助本周验收时才学习；否则记入以后再学，不在本周展开。