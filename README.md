# 2020前端基础知识

## 基础

### JavaScript基础

> 建议每一条都烂熟于心

- 常用设计模式
  - 单例
  - 装饰者
  - 中介者
  - 观察者
  - 迭代器
  
- 装箱 / 拆箱 & 类型转换

- 常用位运算
  
  - 位运算在算法中也可以起到让人眼前一亮的作用，如`~~undefined`
  
- 原型
  - _\_proto__与prototype
  - 顶级原型对象Object
  - Function与Object，鸡生蛋与蛋生鸡问题
  - 原型链继承与类式继承的本质差异, 二者的同名属性分别会如何起作用?
  
- 闭包
  - 实现 & 应用 & 原理
  - 经典问题(`setTimeout` & `IIFE(立即执行函数)` & `let`) 
  
- 执行上下文 调用栈 作用域链
  
  - 推荐阅读我的这篇博客 [搞懂执行上下文+闭包+AO/VO+作用域(链)]([https://linbudu.top/posts/2020/03/17/js%E5%9F%BA%E7%A1%80-%E9%83%A8%E5%88%86.html](https://linbudu.top/posts/2020/03/17/js基础-部分.html))
  - 变量对象(VO)与活动对象(AO)，能把这个说清楚面试官应该就不会在这一块为难你了。同时印象分+++
  
- 继承
  
  - 寄生组合式继承(组合+原型)
  
- 异步 事件循环
  
  - 微任务 & 宏任务 ....
  - 浏览器UI渲染与事件循环?（UI渲染属于哪种任务，它的执行时机？）
  - async与await在其中的处理
  - 实现Promise
  - 并行 顺序 中断 Promise
  - [Promise A+规范](https://segmentfault.com/a/1190000002452115)
    - 立即resolved的Promise执行时机
  
- 垃圾收集
  - 标记清除
  - 引用计数
    - 循环引用如何处理?
  - 引出 -> ES6的WeakSet与WeakMap
  
- this指向
  - 作用 & 意义
  - 隐式丢失
  - 四种优先级
  - 箭头函数的this
  
- Object.defineProperty() 与 descriptor(修饰符，即可配置(**configurable**) 可写(**writable**) 可枚举(**enumerable**) 及值(**value**))

  - 与 Proxy 差异, 为什么Vue3.0切换到Proxy?

- 模块化
  - ES Modules与CommonJS差异
    - 语法 & 导入 & 导出 加载方式
    - 为什么不要使用export default
  - **二者对循环引用的处理**
  - 为什么Webpack要使用摇树优化, 需要将Babel编译结果设置为ES6?
  
- 其他
  
  - call & bind & apply
  
  - caller / callee
  - typeof 与 Instanceof 原理
    - tyoeof null? (机器码)
  - 柯里化(**尾递归优化**) & 函数式编程
  - 类数组
  - isNaN() 和 Number.isNaN()
  - Obejct.is() 的不符直觉的处理（扩展：React的`ShallowEqual`底层对Object.is()进行了优化, 见[shallowEqual.js](https://github.com/facebook/react/blob/a9b035b0c2b8235405835beca0c4db2cc37f18d0/packages/shared/shallowEqual.js)）

### HTML&CSS

> 这一块的话，我的个人想法是不需要准备的太细致，大概的知识点足矣。

- 语义化

- SEO

- DTD `<!DOCTYPE>`

- W3C与WHATWG规范

- Html5新增API

- DOM/BOM API

- 常见布局

- 优先级

- 伪类与伪元素

- 预处理器与后处理器

- 盒模型

- CSS3动画

  - GPU加速原理
  
- 定位

  - 文档流
- 子绝父相 blabla...
  - sticky
  
- src & href 区别

- Flex 布局属性及其可取值

- Rem与em -> 手淘的Flexible方案, 小程序与Rax的rpx方案

- BFC / IFC

- 水平 / 垂直 / 水平垂直居中

- 预处理器与后处理器

- reset与normalize.css, 推荐用哪个?

- 移动端

  - 像素比
  - 检测横屏
  - 图片模糊问题(`srcset`, 自动选择符合像素比的图片)
  
  - 视口类型
  - vw vh
  - 1Px

### 基础手写/算法

> 算法我就帮不上太多忙啦，以下这些，不仅要会基本实现，还要会各个方面的优化版本。

- 原生ajax axios（我有一个仓库是自己实现的axios的http部分，有兴趣的同学可以翻翻，[ts-axios](https://github.com/linbudu599/ts-axios)）
- bind / call / apply
- debounce / throttle
- instanceof
- 深浅拷贝
- promise
- lazy man(挺好玩的)
- new
- 用setTimeout实现setInterval, 为什么要这么做
- 继承
  - 实现ES6 Class实质的继承
- 冒泡 / 快排 / 选择 ...
- 观察者与发布订阅模式
- 刷刷leetcode吧...

### ES6

- let const var 暂时性死区等

- ES6的Class实质, 与ES5继承异同?

  - Babel编译结果
  - 为什么需要先调用`super()`?

- Generator

  - 纤程 & 协程 & 线程 & 进程
  - yield
  - co模块
  
- Iterator

  - for...of

- Symbol类型使用, 一些类库的底层都用它来干什么?

- Promise

  - 回调函数延迟绑定
  - 错误穿透
  - 状态机制

- Async/Await 的原理

  - NodeJS 14.3.0版本实现的顶级await

- Decorator，建议直接看ts的

- Proxy

  - 为什么Vue抛弃了Object.defineProperty
  - 元数据 & 元编程
  - 常用方法

- Reflect

  - 为什么需要它?
  - 与Proxy的结合

- map set

  - map与对象互转
  - set与数组互转

  - weakMap weakSet

- 其他新增API

- 关于TC39的标准制定过程

  - Strawman
  - Proposal
  - Draft
  - Candidate
  - Finished

- ES 7/8/9/10 /...

  - [可选链(Optional-Chaining)](https://github.com/linbudu599/Penumbra)
  - null判断
  - 私有变量
  - 装饰器(ES的实现还没确定下来, 可以看TS的实现)

### Node

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

### 浏览器

- 跨域与跨站

- 强缓存与协商缓存

  - 优先级
  - 请求与响应中的缓存相关请求头

  - E-tag 与 Last-Modified

- 从输入URL到页面呈现

  - 页面渲染中的不良现象
    - 白屏
    - FOUC

  - 图层树 绘制指令 绘制列表
    - 显示提升
    - 隐式提升(层爆炸)

  - 栅格化线程池 位图
  - 重绘 回流
  - DOM树与CSSOM树建树过程
    - 令牌化->建树
    - 样式收集
  - 阻塞
    - js & dom
    - css & js
    - async & defer

- 操作DOM为什么慢?

  - 引擎切换

  - 互斥

- cookie / session / token

  - Chrome80默认cookie samesite属性为Lax, 造成的影响?
    - 推荐阅读: [预测最近面试会考 Cookie 的 SameSite 属性](https://juejin.im/post/5e718ecc6fb9a07cda098c2d)
  - 了解下双令牌机制 `auth_token` & `refresh_token`
  - cookie session_id
  - jsonwebtoken机理

- 本地存储（web storage）

- service worker（随便了解一些即可）

- requesAnimationFrame

- requestIdleCallback（可以在被问到React Fiber时提到）

- 事件机制

  - 委托发生的阶段
  - IE的事件模型
  - 阻止事件与冒泡
  - addEventListener 的第三个参数: useCapture

- RESTFul规范（URL & 方法 & 请求头...）

- 跨域

  - JSONP 原理
  - Nginx 原理 与 实际配置
  - CORS
    - Options预检请求
    - 简单 / 复杂 请求
    - 相关字段

- 前端路由原理

  - hash
    - onHashChange
  - history
    - go
    - push
    - replace
    - pushState
    - replaceState
    - onPopState
  
- XSS

  - 文档型 & 反射型 & 存储型
  - 防范: httpOnly & 转义 & CSP
  
- XSRF

  - GET型 POST型 链接类型

  - 同源检测
    - origin
    - referer
    - 同源检测伪造
  - axios的XSRF防御手段(X-XSRF-TOKEN)
  - samesite！

- Fetch & XHR对比

  - cookie
  - abort
  - 使用`onProgress`监听进度

### 数据库

- 脏读 / 幻读 / 不可重复读
- 事务及边界
- 索引

- ORM(`Object Relationship Mapping`)的原理

### 网络

- 七层与五层模型
- DNS查找机制
  - CDN CNAME
- 请求/响应报文
  - 头 & 主体
- http1.1 -> http1
  - 身份认证
  - 断点续传(206状态码)
  - 缓存
  - keep-alive
- http2 -> http1.1
  - 多路复用
  - 头部压缩
  - server-push
- https 会话层机制
  - (非)对称加密
  - 浏览器预置的CA整数
- TCP 握手/挥手 过程中出错?
- 泛洪攻击
  - RST包
- TCP/UDP适用场景
  - QUIC协议
  - 为什么DNS使用UDP
- TCP拥塞控制
  - 慢启动 & 拥塞避免
  - 快速重传 & 快速恢复
- 正向代理与反向代理
- Get与Post区别
  - 幂等性
  - 安全性

## 进阶

### 框架及工具

#### TypeScript

- type 与 interface 异同

- 类型编程

  > 推荐阅读俺的博客: [TypeScript 类型编程初探](https://linbudu.top/posts/2020/05/30/ts%E7%B1%BB%E5%9E%8B%E7%BC%96%E7%A8%8B%E5%88%9D%E6%8E%A2.html)

  - 泛型
  - 类型守卫 & is关键字 

  - Partial -> 实现递归的Partial

- 装饰器 / IoC体系

- **public / protected / private / static**

#### Git

- 暂存区 等基本概念

- git fetch
- **git rebase**
- git merge
- git reset
- git revert

#### Webpack & Parcel

> Parcel是可选的, 并不需要掌握, 而是作为加分项

- compiler与compilation

- HMR(`Hot Module Reloading`)原理

- 二者的工作流程

- Loader

  - 以Babel-Loader为例, 讲讲loader都做了什么

- Plugin
  
  - Webpack事件流模型 [Tapable](https://github.com/webpack/tapable)
  
- 性能调优
  - 打包速率

    - 减少查找时间
    - DLL(`Dynamic Link Library`, 动态链接库, 已经不推荐使用)

    - 多进程打包插件
    - 影响编译的配置(如`source-map`)

  - 打包大小

    - JS/CSS 摇树优化
    - 压缩 & Uglify
    - 代码分割(`Code Spilting`)

  - 打包交互友好度

    - 进度指示(`webpackbar`插件)
    - 错误友好提示(`friendly-error-plugin`)

#### React

- Redux 与 Mobx 起码熟练一个8

- 生命周期(标注**x**的为已经废弃)

  - WillMount **x**
  - render
  - DidMount
    - 为什么数据获取要在这里? 而不是WillMount?
  - WillReceiveProps **x**
  - shouldComponentUpdate
  - WillUpdate **x**
  - render
  - DidUpdate **x**
  - 以下为新增
  - getDerivedStateFromProps
  - getSnapshotBeforeUpdate
  - getDerivedStateFromError
    - 在页面崩溃时, 与componentDidCatch如何搭配

- 为什么要废弃掉这几个生命周期?

  - 为什么getDerivedStateFromProps是静态方法

- Hooks

  - useEffect
  - useState

  - (可选, 有一定理解难度) forwardRef & useRef & useImperativeHandle

- Fiber

  - requestIdleCallback
- 机制
  - reconciliation 阶段
- commit 阶段
  
- Redux

  - 中间件原理

- setState

  - 原生事件->同步, 合成事件->异步, 为什么?

- React实现的事件机制

- V-Dom与Diff

  - 时间复杂度

- 与Vue的比较

  - 约束 / 迎合开发者
  - 思想

#### Vue

> 实际不止这些 但我不是主要写Vue的

- MVVM原理
  - Observer
  - Compile
  - Watcher

### 业务场景

- 白屏问题排查
- 骨架屏
- 超长列表
  - requesAnimationFrame
  - 虚拟列表
- 单点登录(SSO)
- 埋点的原理
- 扫码登陆
- 大文件分片 / 完整性校验 / 断点续传 / 秒传 / 拖拽上传 / 粘贴上传

### 小程序

- 基础架构
- properties / data
- behavior(封装性)
- DOM BOM是如何禁止访问的?
- 生命周期
  - 页面级
  - 应用级
- 性能优化
- **vs PWA / Hybrid / 各种跨端方案**

## 漫谈

### 测试

- 单元测试
- 集成测试
- 端到端测试(E2E)
- 混沌测试

### 工程化

- 错误监控
  - Sentry原理
  - 你理解的错误监控, 是如何的? 收集哪些信息?
- 性能优化
  - Webpack
  - http缓存
  - 使用**Performance API**获取应用表现
- 脚手架
  - 如何自建脚手架? -> yeoman
- 埋点
  - SPA应用
  - Hybrid应用
- (可选) GraphQL & BFF & Apollo

  - vs RESTFul 优劣势
  - BFF意义, 解决了什么问题?
    - 接口清洗 聚合 ...
    - 带来的新问题
    - Serverless协作
  - Apollo生态圈的主要package
- CI / CD, 自动化构建流程解决了什么问题?
- Serverless

  - FaaS
  - BaaS
  - 小程序云函数思路
  - Serverless解决了什么问题?
- 前端趋势
  - 智能化
  - 跨端
    - 5G 物联网带来的影响
    - Flutter 与 RN此类方案
    - 演进
  - 价值
    - 向后端进发
    - 对业务更熟悉
- 工程化
  - 模块化
    - 以React为例, 你的组件模块化思路?
    - 项目开发模块化
  - 规范化
    - 各种各样的Lint
    - CR
    - 测试
    - ...
  - 系统化
    - 微服务
    - 微前端
    - Serverless
    - 中间层
    - ...
