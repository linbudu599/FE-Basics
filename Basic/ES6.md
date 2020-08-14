# ES6 - Next

- let const var

  - 暂时性死区Temporal Dead Zone
  - 变量提升
  - 块级作用域

- Number.EPSILON，无误差最小值

- 尾调用优化：单项调用帧

  - 尾递归

- Object:

  - keys()
  - values()
  - entries()

- ES6的Class实质, 与ES5继承异同?

  - Babel编译结果分析，见Babel-Playground
  - 为什么需要先调用`super()`?

- Generator

  - 纤程 & 协程 & 线程 & 进程
  - yield
  - co模块
  
- Iterator接口

  - 统一的访问接口（`Symbol.iterator`）与排列顺序

  - 供for...of消费

- Symbol类型使用, 一些类库的底层都用它来干什么?
  
  - 不可使用new关键字，因为不是对象嘛
  - 使用for方法, 使用同一个Symbol值
  - 作为key值, 无法被枚举, 但可以使用`getOwnPropertySymbols()`获取
  
- Promise

  - Promise/A+

  - 回调函数延迟绑定
  - 链式调用
  - 错误穿透
  - 状态机制
  - all race allSettled 及实现
  - 实现并发限制Promise
  - finally()
  - 有一个抛错的promise 在.all中获得正确结果

- Async/Await 的原理

  - NodeJS 14.3.0版本实现的顶级await

- Decorator，建议直接看ts的

- Proxy

  - 为什么Vue抛弃了Object.defineProperty
  - 元数据 & 元编程
  - revocable() -> { proxyInstance, revoke }
    - Immer中的使用

- Reflect

  - 设计目的
    - 函数式操作
    - 更合理的行为

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

  - Promise.allSettled() resolve与reject都会返回
  
  - Dynamic Import: import()
  
  - [可选链(Optional-Chaining)](https://github.com/linbudu599/Penumbra) `a?.b?.c`
  - null判断运算符（空值合并） `null ?? "default" `  
  - 私有变量
  - 装饰器(ES的实现还没确定下来, 可以看TS的实现)，但是ES现在的装饰器提案感觉越变越诡异了，所以不要以TS的装饰器为准。
  - 第七种原始类型 `BigInt`
  - `Array.flat()`
  - `Object.fromEntries()`
  - 稳定的`Array.sort()`方法 （稳定：键值相等的对象排序前后顺序相同）
  - `export * as otherName from "../xx"`

