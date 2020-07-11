# 漫谈

## 测试

- 单元测试
  - Jest
  - Mocha
- 集成测试
  - React-Testing-Library
  - Enzyme
- 端到端测试(E2E)
  - Puppeteer

## 工程化

- 错误监控

  - Sentry 原理, 重写?方法
  - 你理解的错误监控是如何的? 收集哪些信息? 如何上报?
    - Web 埋点
    - 客户端埋点

- 性能优化

  - Webpack
  - http 缓存
  - 使用**Performance API**获取应用表现并针对性的进行优化
  - 针对框架的性能优化, 如上面提到的 React

- 脚手架

  - 如何自建脚手架? -> yeoman
  - 自建脚手架的思路, 类似 Feflow

- (可选) GraphQL & BFF & Apollo

  - vs RESTFul 优劣势
  - BFF 意义, 解决了什么问题?
  - 接口清洗 聚合 胶水层...
  - 带来的新问题
  - **FaaS** + **BFF**! 现在你不需要担心自己的胶水层顶不住流量了
  - GraphQL-Client, **Apollo** or **Relay**?

- CI / CD, 自动化构建流程解决了什么问题?

  - GitHub Actions
  - Travis
  - CircleCI

- Serverless

  - **Serverless 解决了什么问题...?**

  - FaaS
    - 冷启动 & NodeJS 冷启动优势(V8 JIT)
    - 即用即毁 & 常驻进程
    - 触发器
    - FaaS 分层: 容器 runtime 代码
    - 横向 & 纵向缩扩容
  - BaaS
  - BFF & SFF
  - Midway-FaaS
  - 小程序云函数思路

- 前端趋势

  - 智能化 如 Imgcook
  - 跨端
    - 5G 物联网带来的影响
    - Flutter / RN / Taro / Rax / ...
    - 演进
  - 前端工程师的自我定位与市场定位
  - 技能深度 & 广度

- 工程化
  - 模块化
    - 以 React 为例, 你的组件模块化思路?
    - Rax 开发的模块化
  - 规范化
    - 各种各样的 Lint
    - Pre-Commit Hook(`Husky` + `Lint-Staged`)
    - Code Review
    - 规范的测试!
  - 系统化
    - 微服务
    - 微前端
    - Serverless
    - BFF 中间层
    - ...
