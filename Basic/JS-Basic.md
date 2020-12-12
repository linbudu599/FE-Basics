# JavaScript基础

- 常用设计模式
  - 单例
  - 装饰者
  - 中介者
  - 观察者
  - 迭代器
  - 设计模式的实际应用
  
- 装箱 & 拆箱 & 类型转换

- 数据类型判断

  - typeof 基于底层机器码的判断 对于对象不准确(都会显示object)
- typeof
  - instanceof 基于原型链的判断 可准确判断Array/Function/Object
- 对于基本数据类型?
    - 111 instanceof Number -> false 字面量值(111) 与 实例(new Number())的不同
- constructor 同样可以理解为基于原型链, 但修改原型会使得结果不准确
  - **Object.prototype.toString.call()**  最准确的判断 可用于深拷贝中判断数据类型, 返回`"[object array]"`这种形式
  
- 常用位运算
  
  - 位运算在算法中也可以起到让人眼前一亮的作用，如`~~undefined -> 0`
  
- 原型与原型链
  
  - 原型链的设计初衷
  
  - _\_proto__与prototype
  
  - 顶级原型对象Object
  
  - Function与Object，鸡生蛋与蛋生鸡问题
  
  - 原型链继承与类式继承的本质差异, 二者的同名属性分别会如何起作用?
  
    > 两种继承的多态分别如何体现
  
  - ES6的Class与原型链的关系(编译结果中静态成员 与 实例成员的添加方式)
  
    > 可阅读 [从Babel编译结果看ES6的Class实质](https://linbudu.top/posts/2020/03/25/babel-class.html)
  
- 闭包
  - 实现 & 应用 & 原理
  - 经典问题 setTimeout + for循环
  - 尝试使用一句话通俗的讲清闭包概念
  
- 执行上下文

  > [搞懂执行上下文+闭包+AO/VO+作用域(链)]([https://linbudu.top/posts/2020/03/17/js%E5%9F%BA%E7%A1%80-%E9%83%A8%E5%88%86.html](https://linbudu.top/posts/2020/03/17/js基础-部分.html))

  - 变量对象(VO)与活动对象(AO)
  - 调用栈
  - 作用域链
  - 扩展: 尾递归优化

- 继承
  
  - 寄生组合式继承(组合+原型)
  
- 异步 事件循环
  
  - 微任务 & 宏任务
  - 浏览器UI渲染与事件循环?（UI渲染属于哪种任务，它的执行时机？）
  - async与await在其中的处理
  - 可扩展至NodeJS的事件循环
  
- Promise
  
  - 实现Promise(race/all(并发限制版)/abort/allSettled...)
  - 并行 顺序 中断 Promise
  - [Promise A+规范](https://segmentfault.com/a/1190000002452115)
    - 立即resolved的Promise执行时机 >>> 事件循环
  
- 垃圾收集
  
  - 内存泄漏(如何使用Chrome排查)
  
  - 标记清除
  - 引用计数
    - 循环引用如何处理?
  - 扩展 -> ES6的WeakSet与WeakMap设计原因
  
- this指向
  - 作用 & 意义
  - 隐式丢失
  - 四种优先级
  - 箭头函数的this
  
- Object.defineProperty() 与 descriptor(修饰符，即可配置(**configurable**) 可写(**writable**) 可枚举(**enumerable**) 及值(**value**))

  - 与 Proxy 差异, 为什么Vue3.0切换到Proxy? 这解决了Vue2.x的哪些问题?

- 模块化
  
  - AMD UMD ...
  - ES Module与CommonJS差异
    - 语法 & 导入 & 导出 & 加载方式
    - export default可能存在的问题
  - **二者对循环引用的处理**
  - 为什么Webpack使用摇树优化, 需要将Babel编译结果设置为ES6?
  
- 其他

  - new操作进行的步骤

  - call & bind & apply
  - caller / callee
  - 柯里化(**尾递归优化**) & 函数式编程
  - 类数组
  - isNaN() 和 Number.isNaN()
  - Obejct.is() 的不符直觉的处理（扩展：React的`ShallowEqual`底层对Object.is()进行了优化, 见[shallowEqual.js](https://github.com/facebook/react/blob/a9b035b0c2b8235405835beca0c4db2cc37f18d0/packages/shared/shallowEqual.js)）
  - 深浅拷贝
    - ...运算符
    - JSON.parse(JSON.stringify())
    - 真-深拷贝
