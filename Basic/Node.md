# Node

- 优缺点 适用场景
  - Nginx也是事件驱动
- 进程 & 线程，单线程
- Node创建子进程的方式，这几种方式的底层，异同
  - spawn
  - exec
  - execFile
  - fork
- child_process与cluster: 多进程模型，以多进程的方式模拟多线程
- worker_threads: 真·多线程
- 多进程：需要IPC，CPU利用率低（切换复杂），编码与调试方便，进程独立。
- 多线程：利用率高，编码调试复杂，线程影响。
- npm install过程
- npm script
  - pre & post
  - npm ci: 根据lock文件安装，且安装确切版本而非计算依赖，加速安装过程。删除已有的模块目录。不会写入package.json
  - npm i eslint-{plugin-import,plugin-react,loader} express
  - npm run env -> process.env.xxx
  - && 串行 与 & 并行
  - npm docs / npm home / npm repo  导航至文档/仓库
  - npm dedupe(ddp) 删除重复依赖
  - npm audit 扫描依赖漏洞 fix: 安装所有漏洞包的补丁版本
  - npm doctor
  - npm link 本地调试包
  - npm list
  - npm outdated --long / npm outdated -l 列举过时依赖

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
- 服务端渲染(SSR)

  - SEO
  - 首次有效渲染
  - **同构**
  - 使用到的React API
  - 数据注水 & 脱水
