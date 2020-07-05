# Node

- 优缺点 适用场景

- Node创建子进程的方式，这几种方式的底层，异同
  - spawn
  - exec
  - execFile
  - fork
  
- npm install过程

  - 版本冲突 与 dedupe
  
- Buffer

- Stream
  
  - 可读/可写/可读可写/可转换流
  
- Node的适用场景及原因（事件驱动 异步I/O blabla...）

- V8内存管理

  - 新生代与老生代机制
    - From空间与To空间
  - 标记清除与标记整理
    - 触发点
  - 增量标记
  
- Cluster & IPC

  - child_progress
  - 主从模式
  
- Node异步I/O & 进程池 & Libuv

- 事件循环

  - timer
  - I/O
  - Idle prepare
  - poll
    - 阻塞
  - check
  - close CB
  - 每一阶段均有的nextTick与microTask
  
- Koa

  - vs Express: 异同点 & 各自优势
  - 中间件原理 与 洋葱模型(Koa-Compose模块)
  - 选择Koa与选择Express的考量权衡