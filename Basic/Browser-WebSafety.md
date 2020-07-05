# 浏览器 & Web安全

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
    - 加载js 阻塞 dom
    - css & js的加载
    - 给js标签添加async & defer的作用

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