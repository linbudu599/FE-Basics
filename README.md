# 2020前端基础知识

> 适用于20/21届前端同学

## 基础

### JavaScript基础

- 装箱 / 拆箱 & 类型转换
- 原型
  - _\_proto__与prototype
  - Object.prototype
  - Function与Object
- 闭包
  - 实现
  - 应用
  - 原理
  - 经典问题(`setTimeout` `IIFE` `let`) 
- 执行上下文 调用栈 作用域链
  - 变量对象(VO)与活动对象(AO)
- 继承
  - 寄生组合式继承(组合+原型)
- 事件循环
  - 浏览器UI渲染与事件循环?
  - async与await
  - Promise/A+规范
    - 立即resolved的Promise执行时机
- 垃圾收集
  - 标记清除
  - 引用计数
    - 循环引用如何处理?
- this
  - 作用 & 意义
  - 隐式丢失
  - 优先级
  - 箭头函数的this
- 对象冻结
  - freeze
  - seal
- Object.defineProperties() 与 descriptor
- 模块化
  - ES Modules与CommonJS差异
  - 对循环引用的处理

- 其他
  - caller / callee
  - typeof 与 Instanceof 原理
    - tyoeof null? (机器码)
  - 柯里化
    - 尾递归
  - 类数组
  - isNaN 和 Number.isNaN
  - Obejct.is()漏洞
    - React 使用的 `shallowEqual()` 对其进行的增强

### HTML&CSS

- DTD `<!DOCTYPE>`
- W3C与WHATWG
- Html5新增API

- DOM/BOM API
- 常见布局

- 优先级

- 盒模型

- CSS3动画

  - GPU加速原理

- 定位

  - 文档流

  - sticky

- src & href

- Flex

- Grid

- Rem与em

- Flexible.js思路

- BFC / IFC

- 水平 / 垂直 / 水平垂直居中

- Prefix

- reset与normalize.css

- 移动端

  - 像素比
  - 检测横屏
  - 图片模糊问题

  - IOS橡皮筋问题
  - 视口类型
  - Vw Vh
  - 1Px

### 基础手写/算法

- bind / call / apply
- debounce / throttle
- instanceof
- 深浅拷贝
- promise
- lazy man
- new
- 用setTimeout实现setInterval
- 继承
  - 实现ES6 Class实质的继承
- 冒泡 / 快排 / 选择 ...
- 观察者与发布订阅模式

### ES6

- ES6的Class实质, 与ES5继承异同?

  - Babel编译结果
  - 为什么先`super()`?

- Generator

  - 协程
  - yield
  - co模块
  - Thunk函数

- Iterator

  - for...of

- Symbol

  - 常用的内置接口

- ES6 Module与CommonJS

- Promise

  - 回调函数延迟绑定
  - 错误穿透
  - 状态机制

- Async/Await 的原理

- Decorator

- Proxy

  - 为什么Vue抛弃了Object.defineProperty
  - 元编程
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
  - Canidate
  - Finished

- ES 7/8/9/10 /...

  - 可选链
  - null判断
  - 私有变量
  - ...

### Node

- 优缺点 适用场景
- Node创建子进程的方式
  - spawn
  - exec
  - execFile
  - fork

- npm install

  - dedupe

- Buffer

- Stream

- Node的适用场景及原因

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

  - vs Express?

  - 中间件原理 与 洋葱模型

### 浏览器

- 强缓存与协商缓存

  - 优先级
  - 请求与响应中的缓存相关请求头

  - E-tag 与 Last-Modified

- 从输入URL到页面呈现

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

- cookie / session / token

  - Chrome80默认cookie samesite属性为Lax, 造成的影响?
    - 如何解决兼容性
  - 双令牌机制
  - cookie session_id
  - jwt机理

- mainiest

- service worker

- requesAnimationFrame

- requestIdleCallback

- 事件机制

  - 委托发生的阶段
  - IE的事件模型
  - 阻止事件与冒泡
  - addEventListener & useCapture

- 跨域

  - JSONP 原理
  - Nginx 原理
  - CORS
    - Options预检
    - 简单 / 复杂 请求
    - 相关字段

- 前端路由原理

  - hash
    - onHashChange
  - history
    - pushState
    - replaceState
    - onPopState

- XSS

  - 文档型 & 反射型 & 存储型
  - httpOnly
  - 转义
  - CSP

- XSRF

  - GET型 POST型 链接类型

  - 同源检测
    - origin
    - referer
  - axios的XSRF防御手段
  - samesite

- Fetch & XHR对比

  - cookie
  - abort
  - onProgress

### 数据库

- 脏读 / 幻读 / 不可重复读
- 事务及边界
- 索引



### 网络

- 七层与五层模型
- DNS查找机制
  - CDN CNAME
- http1.1 -> http1
  - 身份认证
  - 断点续传(206状态码)
  - 缓存
  - keep-alive
- http2 -> http1.1
  - 多路复用
  - 头部压缩
  - server-push
- https 会话层机制?
  - 浏览器内置CA链
- TCP 握手/挥手 过程中出错?
- 泛洪攻击
  - RST包
- TCP/UDP适用场景
  - QUIC协议
- TCP拥塞控制
  - 慢启动 & 拥塞避免
  - 快速重传 & 快速恢复

## 进阶

### 框架及工具

#### TypeScript

- type & interface
- 泛型
- 工具类型
- 类型守护
- 装饰器 / IOC

#### Git

- git fetch
- git rebase
- git merge
- git reset
  - hard
  - soft
  - mixed
- git revert

#### Webpack & Parcel

- compiler与compilation
- HMR原理
- 工作流程
- Loader
  - 以Babel-Loader为例
- Plugin
  - 事件流模型
- 性能调优
  - 打包速率
  - 打包大小
  - 打包交互友好度
- 异同

#### React

- Immutable.JS

- 生命周期

  - WillMount x
  - render
  - DidMount
    - 为什么数据获取要在这里? 而不是WillMount?
  - WillReceiveProps x
  - shouldComponentUpdate
  - WillUpdate x
  - render
  - DidUpdate x
  - 以下为新增
  - getDerivedStateFromProps
  - getSnapshotBeforeUpdate
  - getDerivedStateFromError
    - 与componentDidCatch如何搭配

- 为什么要废弃掉这几个生命周期?

  - 为什么getDerivedStateFromProps是静态方法

- Hooks

  - useEffect
  - useState

  - forwardRef & useRef & useImperativeHandle

- Fiber

  - requestIdleCallback

  - 机制

  - reconciliation / commit

- Redux

  - 中间件原理

- setState

  - 原生事件->同步, 合成事件->异步, 为什么?

- React实现的事件机制

- V-Dom与Diff

  - 时间复杂度

- 与Vue的比较

  - 约束 / 迎合
  - 思想

#### Vue

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
- 大文件分片/完整性校验/断点续传/秒传/拖拽上传/粘贴上传

### 小程序

- 基础架构
- properties / data
- behavior

- DOM BOM如何禁止访问的?
- 生命周期
- 性能优化
- **vs PWA / H5 / Hybrid / 各种跨端方案**

## 漫谈

### 测试

- 单元测试
- E2E
- 混沌

### 工程化

- 错误监控
- 性能优化
- 脚手架
- 埋点
  - SPA应用
  - Hybrid应用
- GraphQL & BFF & Apollo

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
- 前端趋势
  - 智能化
  - 跨端
    - 5G 物联网
    - Flutter 与 RN此类方案
    - 演进
  - 价值
    - 向后端侵袭
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
    - Serverless
    - 中间层
    - ...