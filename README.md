# 2020 前端基础知识

## 基础

### [JavaScript 基础](./Basic/JS-Basic.md)

### [HTML & CSS 基础](./Basic/HTML-CSS.md)

### [基础手写/算法](./Basic/HandWritting.md)

### [ES6 基础](./Basic/ES6.md)

### [Node 基础](./Basic/Node.md)

### [浏览器 & Web 安全](./Basic/Browser-WebSafety.md)

### [数据库](./Basic/Database.md)

### [网络](./Basic/Network.md)

## 进阶

### 性能优化

- **First Pain**: 首次绘制，即页面第一次绘制像素的时间，越快越好
- **First Contentful Paint**: 页面第一次绘制文本/图片等非空元素的时间，越快越好
- **Largest Contentful Paint**: 视窗内最大元素绘制时间，会随着渲染过程变化（大元素可能会发生改变），会在用户第一次交互后停止记录。官方推荐在**2.5s**内为优秀，**2.5s-4s**为需要改进，比FP与FCP更能体现用户页面体验。
- **Time to Interactive**: 首次可交互时间，重要指标，代表页面进入真正可用状态。
- **First Input Delay**: 首次输入延迟， FCP与TTI之间用户首次与页面交互时3的响应延迟。
- **Cumalative Layout Shift**: 页面非预期位移波动，如影响体验的大块内容插入。
- 基于[Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)获取指标
- 资源大小及加载速度&网络速度：FP FCP LCP

### [TypeScript](./Advanced/Ts.md)

### Git

- 暂存区 等基本概念&命令
- git fetch
- **git rebase**
- git merge
- git reset
- git revert
- git branch 相关
- Git Flow 工作流

### Babel

- 工作阶段
  - 解析 babylon
  - 转化 babel-traverse
  - 生成 babel-generator
- babel-plugin
- babel-preset
- babel-polyfill
- @babel/plugin-transform-runtime

### [Webpack & Parcel](./Advanced/Webapck-other.md)

### [React](./Advanced/React.md)

### [业务场景](./Advanced/Reality.md)

### 小程序

- 基础架构
- properties / data
- behavior(封装性)
- DOM BOM 是如何禁止访问的?
- 生命周期
  - 页面级
  - 应用级
- 性能优化
- vs PWA / Hybrid / RN / Flutter ...

## [漫谈](./Advanced/Wonder.md)
