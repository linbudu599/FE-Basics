# 2020前端基础知识

## 基础

### [JavaScript基础](./Basic/JS-Basic.md)

### [HTML & CSS基础](./Basic/HTML-CSS.md)

### [基础手写/算法](./Basic/HandWritting.md)

### [ES6基础](./Basic/ES6.md)

### [Node基础](./Basic/Node.md)

### [浏览器 & Web安全](./Basic/Browser-WebSafety.md)

### [数据库](./Basic/Database.md)

### [网络](./Basic/Network.md)

## 进阶

### TypeScript

- type 与 interface 的异同点

- Class增强 -> 关键字

- 类型编程

  > 推荐阅读俺的博客: [TypeScript 类型编程初探](https://linbudu.top/posts/2020/05/30/ts%E7%B1%BB%E5%9E%8B%E7%BC%96%E7%A8%8B%E5%88%9D%E6%8E%A2.html)

  - 泛型
  - 类型守卫 & is关键字

  - 实现工具类型

- 装饰器 / IoC体系

- **public / protected / private / static**关键字

#### Git

- 暂存区 等基本概念
- git fetch
- **git rebase**
- git merge
- git reset
- git revert
- Git Flow工作流

## Babel

- 工作阶段
  - 解析 babylon
  - 转化 babel-traverse
  - 生成 babel-generator
- babel-plugin
- babel-preset
- babel-polyfill
- @babel/plugin-transform-runtime

#### Webpack & Parcel

> Parcel是可选的, 并不需要掌握, 而是作为加分项

- compiler与compilation, Webpack构建流程

- HMR(`Hot Module Reloading`)原理

- 二者的工作流程

- Loader

  - 以Babel-Loader为例, 讲讲loader都做了什么

- Plugin
  
  - Webpack事件流模型 [Tapable](https://github.com/webpack/tapable)
  
- 性能调优
  - 打包速率

    - 减少查找时间 -> 在loader中针对性的exclude掉无关文件夹, 比如在url-loader/file-loader处理图片的配置你就可以把assets以外的目录去掉, 蚊子腿再小也是肉!
    - DLL(`Dynamic Link Library`, 动态链接库, 已经不推荐使用)

    - 开启多进程打包
    - 影响编译速度的配置(如`source-map`)

  - 打包大小

    - JS/CSS 摇树优化 按需加载
    - 压缩 & Uglify(`Terser`)
    - 代码分割(`Code Spilting`), 讲讲`SplitChunksPlugin`, 讲讲Dynamic Import

  - 打包交互友好度(可选, 但很好玩hhh)

    - 进度指示(`webpackbar`)
    - 错误友好提示(`friendly-errors-plugin`)

#### React

- 性能优化

  - 分析问题: React Devtools的`Highlight Update`与`Profiler`, Chrome的`Performance`工具

  - 阻止无意义的重渲染, 通常通过缓存/更新控制(`useMemo`/`shouldComponentUpdate`)
  - 懒加载(`React-Loadable` & `Suspense` + `React.lazy()`)
  - 细粒度更新
  - 谨慎使用Context或基于Context的数据流方案
  - 不可变数据
  - React Hooks!
  - 不可变数据, `ImmerJS` / `ImmutableJS`
  - 减少不必要的重新计算, 如`useCallback`与`Reselect`
  - 虚拟列表

- 生命周期, 按照顺序, 废弃原因可以参见 [React16.4生命周期初探](https://linbudu.top/posts/2020/06/29/react-life-cycle.html)

  - 挂载
    - **constructor**
    - **static getDerivedStateFromProps**
    - **componentWillMount** **已废弃**
    - **render**
    - **componentDidMount** 为什么数据获取要在这里? 而不是WillMount?
  - 更新
    - **componentWillReceiveProps** **已废弃**
    - **static getDerivedStateFromProps**
    - **shouldComponentUpdate**
    - **componentWillUpdate** **已废弃**
    - **render**
    - **static getSnapshotBeforeUpdate**
    - **componentDidUpdate**
  - 错误

  - **static getDerivedStateFromError**, 在页面崩溃时, 与`componentDidCatch`如何搭配降级?

- 为什么要废弃掉这几个生命周期?

- 为什么新增的生命周期是静态方法?

- Hooks

  - useState
- useEffect
  - (可选, 有一定理解难度) forwardRef & useRef & useImperativeHandle
  - useCallback
  - useMemo
  - useRef, 可用于解决闭包陷阱, 缓存等

- Fiber

  - reconciliation
  - commit
  - Concurrent模式
    - Suspense
    - useTransition

- Redux 与 Mobx 起码熟练一个8

  - 源码
- 中间件原理
  
- 其他数据流方案, 如**Dva/Icestore/Hox...** 略有涉猎即可

- setState, 原生事件->同步, 合成事件->异步, 为什么?

- React的合成事件机制(为什么Class组件要bind方法的原因)

- V-Dom与Diff算法

- 与Vue的比较

  - 约束 / 迎合开发者
  - 思想
  
- React-Router(Reach-Router)等路由方案



#### Vue

> 实际不止这些 但我不是主要写Vue的

- MVVM原理
  - Observer
  - Compile
  - Watcher
- Vue 3.0 为什么使用Proxy? 相比defineProperty有什么优势?



### 业务场景

- 页面优化
  - 性能
  - SSR
  - OPR（离线预渲染）
- 白屏问题排查
  - IP地址
  - 日志
  - 路由
  - 请求返回
- 骨架屏
- 超长列表
  - requesAnimationFrame
  - 虚拟列表
- 埋点
  - 部分埋点
  - 可视化埋点
  - 全埋点
  - 设计埋点SDK
- 扫码登陆
  - 长连接
- 文件上传
  - <form> & multipart/form-data & POST
  - [File MIME](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Basics_of_HTTP/MIME_types)
  - koa-body
  - 进度监听 xhr.upload.onprogress
  - 取消 xhr.abort()
  - 预览 window.URL.createObjectURL
  - 拖拽上传 dragover drop dragleave drop事件中e.dataTransfer.files
  - 剪贴板上传 contenteditable paste事件 event.clipboardData(window.clipboardData) getAsFile 
- 大文件上传
  - Blob.prototype.slice() 文件块标志（时间戳/索引） 合并告知请求 服务端合并文件
  - TCP并发控制
  - 服务端stream + pipe
- 断点续传
  - spark-md5 contenthash webworker，本地保存已上传切片信息，重新上传时比对hash值


### 小程序

- 基础架构
- properties / data
- behavior(封装性)
- DOM BOM是如何禁止访问的?
- 生命周期
  - 页面级
  - 应用级
- 性能优化
- vs PWA / Hybrid / RN / Flutter ...



## 漫谈

### 测试

- 单元测试
  - Jest
  - Mocha
- 集成测试
  - React-Testing-Library
  - Enzyme
- 端到端测试(E2E)
  - Puppeteer



### 工程化

- 错误监控
  - Sentry原理, 重写?方法
  - 你理解的错误监控是如何的? 收集哪些信息? 如何上报?
    - Web埋点
    - 客户端埋点
  
- 性能优化
  - Webpack
  - http缓存
  - 使用**Performance API**获取应用表现并针对性的进行优化
  - 针对框架的性能优化, 如上面提到的React
  
- 脚手架
  
  - 如何自建脚手架? -> yeoman
  - 自建脚手架的思路, 类似Feflow
  
- (可选) GraphQL & BFF & Apollo

  - vs RESTFul 优劣势
  - BFF意义, 解决了什么问题?
  - 接口清洗 聚合 胶水层...
  - 带来的新问题
  - **FaaS** + **BFF**!  现在你不需要担心自己的胶水层顶不住流量了
  - GraphQL-Client, **Apollo** or **Relay**?

- CI / CD, 自动化构建流程解决了什么问题?

  - GitHub Actions
  - Travis
  - CircleCI

- Serverless

  - **Serverless解决了什么问题...?**
  
  - FaaS + BaaS
  - Midway-FaaS
  - 小程序云函数思路
  
- 前端趋势
  - 智能化 如Imgcook
  - 跨端
    - 5G 物联网带来的影响
    - Flutter / RN / Taro / Rax
    - 演进? 
  - 自我定位与市场定位
  - 技能深度 & 广度

- 工程化
  - 模块化
    - 以React为例, 你的组件模块化思路?
    - Rax开发的模块化
  - 规范化
    - 各种各样的Lint
    - Pre-Commit Hook(`Husky` + `Lint-Staged`)
    - Code Review
    - 规范的测试!
  - 系统化
    - 微服务
    - 微前端
    - Serverless
    - BFF中间层
    - ...
