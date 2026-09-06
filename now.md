# 本周：ThreadPool v0

## 本周交付
实现一个支持多 worker、阻塞等待、future 和优雅关闭的 C++17 线程池。

## 每日任务
- [ ] Day 1：线程安全队列（push/pop）与 3 个测试
- [ ] Day 2：单线程任务执行器，支持 lambda
- [ ] Day 3：多 worker 与 mutex 保护
- [ ] Day 4：condition_variable 阻塞等待和唤醒
- [ ] Day 5：submit()、future 与异常传递
- [ ] Day 6：优雅停止与资源回收
- [ ] Day 7：benchmark、README 与复盘

## 验收
- [ ] 1,000 个任务正确执行
- [ ] submit() 能返回 future
- [ ] 异常能从 future 取回
- [ ] stop() 后无死锁
- [ ] README 包含架构、用法、测试与 benchmark

## 今天
- [ ] 实现 ThreadSafeQueue
- [ ] 为 push/pop 写测试
