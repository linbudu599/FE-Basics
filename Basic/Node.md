# Node

- Node架构：标准库 - Node Bindings - V8 & Libuv & C-ares & http_parser & zlib...

- GC

  - 标记清除：全部标记 - 清除运行及被运行引用 - 清除带有标记的
  - 引用计数  循环引用

  - 新生代: Scavenge算法，From空间 To空间
  - 对象晋升到老生代条件

  - 老生代

  	- 标记-清除

  	- 标记整理

  	- 增量标记
- 架构
  - Node标准库（JS）
  - Node Binding(C++)
  - **V8** + C-ares + Http-Parser + Zlib + **Libuv**

- 优缺点 适用场景

  - 高性能
  - 非阻塞I/O + 事件驱动模型
  - 单线程
  - 适用于I/O密集型应用，不适用于CPU密集型，因为单线程可能会导致线程卡住

- Nginx也是事件驱动

- 进程 & 线程，单线程

  - Node创建子进程的方式，这几种方式的底层，异同

    - spawn
    - exec
    - execFile
    - fork
- `child_process`与`cluster`: 多进程模型，以多进程的方式模拟多线程
  
  - `worker_threads`: 真·多线程
- 多进程：需要IPC，CPU利用率低（切换复杂），编码与调试方便，进程独立。
  
- 多线程：利用率高，编码调试复杂，线程影响。
  
- `exports` 与 `module.exports`

- npm install过程

  - 确定首层依赖，以工程本身作为依赖树根节点，Node开启多进程寻找深层节点
  - 获取模块信息 - 获取模块实体（检查缓存） - 查找是否有依赖 - 递归或回到上一步
  - dedupe（flat / 扁平化）遍历所有节点，将依赖都放在根节点下，将模块名相同且在兼容范围内的重复依赖去掉，否则留在自己的依赖树里。
  - 更新node_modules，执行生命周期。

- npm script
  - pre & post 钩子
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
  
- 错误优先的回调函数风格

- V8内存管理GC

  - V8内存限制，64位1.4G，32位0.7G（1.5GB执行一次GC需要50ms以上（增量式），甚至可能达到1s（非增量））
  - Scavenge算法

  - 新生代与老生代机制
  - From空间与To空间
  - 标记清除与标记整理
    - 触发点
  - 增量标记
  - 内存泄漏 排查
    - Express / Koa项目

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

