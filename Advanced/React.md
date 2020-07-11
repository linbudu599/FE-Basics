# React

- 性能优化

  - pureComponent shallowEuqal
  - React.memo
  - 分析问题: React Devtools 的`Highlight Update`与`Profiler`, Chrome 的`Performance`工具

  - 阻止无意义的重渲染, 通常通过缓存/更新控制(`useMemo`/`shouldComponentUpdate`)
  - 懒加载(`React-Loadable` & `Suspense` + `React.lazy()`)
  - 细粒度更新
  - 谨慎使用 Context 或基于 Context 的数据流方案
  - 不可变数据
  - React Hooks!
    - useRef
    - useMemo
    - useCallback
    - 自定义 hooks 来封装逻辑
  - 不可变数据, `ImmerJS` / `ImmutableJS`
  - 减少不必要的重新计算, 如`useCallback`与`Reselect`
  - 虚拟列表

- 生命周期, 按照顺序, 废弃原因可以参见 [React16.4 生命周期初探](https://linbudu.top/posts/2020/06/29/react-life-cycle.html)

  - 挂载
    - **constructor**
    - **static getDerivedStateFromProps**
    - **componentWillMount** **已废弃**
    - **render**
    - **componentDidMount** 为什么数据获取要在这里? 而不是 WillMount?
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
  - Concurrent Mode
    - Suspense
      - Suspense 编排 资源竞态控制 见[聊聊 Concurrent 模式中的 Suspense](https://linbudu.top/posts/2020/07/06/concurrent-suspense.html)
    - useTransition

- Redux 与 Mobx 起码熟练一个 8

  - 源码! 看看吧 真不多不难
  - 中间件原理
  - 其他数据流方案, 如**Dva/Icestore/Hox...** 略有涉猎即可

- 不可变数据

  - ImmerJS
  - ImmutableJS

- setState, 原生事件->同步, 合成事件->异步, 为什么?

- React 的合成事件机制(为什么 Class 组件要 bind 方法的原因)

- V-Dom 与 Diff 算法

- 与 Vue 的比较

  - 约束 / 迎合开发者
  - 思想

- React-Router(Reach-Router)等路由方案

#### Vue

> 实际不止这些 但我不是主要写 Vue 的

- MVVM 原理
  - Observer
  - Compile
  - Watcher
- Vue 3.0 为什么使用 Proxy? 相比 defineProperty 有什么优势?
