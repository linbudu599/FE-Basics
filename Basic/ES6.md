# ES6

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
  
  - 不可使用new关键字
  - description
  - 使用for方法, 使用同一个Symbol值
  - 作为key值, 无法被枚举, 但可以使用`getOwnPropertySymbols()`获取

- Promise

  - 回调函数延迟绑定
  - 错误穿透
  - 状态机制
  - all race allSettled

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