# 浏览器 & Web 安全

- 跨域与跨站

- 强缓存与协商缓存

  - 优先级
  - 请求与响应中的缓存相关请求头

  - E-tag 与 Last-Modified

- prepload & prefetch(低优先级,在后台下载)

- DNS prefetching <\link rel="dns-prefetch" />

- 从输入 URL 到页面呈现

  - 页面渲染中的不良现象

    - 白屏
    - FOUC

  - 图层树 绘制指令 绘制列表

    - 显示提升
    - 隐式提升(层爆炸)

  - 栅格化线程池 位图
  - 重绘 回流
  - DOM 树与 CSSOM 树建树过程
    - 令牌化->建树
    - 样式收集
  - 阻塞
    - 加载 js 阻塞 dom
    - css & js 的加载
    - 给 js 标签添加 async & defer 的作用

- 操作 DOM 为什么慢?

  - 引擎切换

  - 互斥

- cookie / session / token

  - Chrome80 默认 cookie samesite 属性为 Lax, 造成的影响?
    - 推荐阅读: [预测最近面试会考 Cookie 的 SameSite 属性](https://juejin.im/post/5e718ecc6fb9a07cda098c2d)
    - 啊哦, Chrome83 又把这个属性默认值回滚了(因为考虑到新冠肺炎的影响), 最早恢复也要在 84 版本了(大概七月下旬)
  - 双令牌机制 `auth_token` & `refresh_token`
  - cookie session_id
  - jsonwebtoken 机理

- 本地存储（web storage）

- service worker（随便了解一些即可）

- requesAnimationFrame

  - 动画的循环时间间隔难以确定, 如果过短会导致浏览器重绘频率极限(16ms).
  - 定时器只是指示多久以后将动画任务添加到 UI 线程任务队列中,不一定会被立刻执行
  - rAF: 自动优化性能(不可见时不执行) & 绘制间隔为浏览器刷新频率
  - 回调会在每一帧保证执行

- requestIdleCallback（可以在被问到 React Fiber 时提到）

  - 不会保证被执行
  - 只有在每一帧有空闲时间时间时执行

- 事件机制

  - 委托发生的阶段
  - IE 的事件模型
  - 阻止事件与冒泡
  - addEventListener 的第三个参数: useCapture

- RESTFul 规范（URL & 方法 & 请求头...）

- 跨域

  - JSONP 原理
  - Nginx 原理 与 实际配置
  - CORS
    - Options 预检请求
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

  - GET 型 POST 型 链接类型

- 同源检测

  - origin
  - referer
  - 同源检测伪造
  - axios 的 XSRF 防御手段(X-XSRF-TOKEN)
  - samesite！

- Fetch & XHR 对比

  - cookie
  - abort
  - 使用`onProgress`监听进度
