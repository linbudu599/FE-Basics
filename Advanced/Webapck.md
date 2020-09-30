# Webpack & Parcel

> Parcel 是可选的

- compiler 与 compilation, Webpack 构建流程

- HMR(`Hot Module Reloading`)原理

- Webpack 构建流程

  - 校验配置文件, 生成本次构建配置及初始化Compiler对象 & Compilation实例
  - 解析文件,生成依赖关系图, 依次执行loader
  - 递归解析处理依赖, 生成chunk, 拼接文件
  - 过程中plugin会在tapable的钩子上被调用

- Plugin生命周期
- Parcel 构建流程

  - @parcel/transformer-xxx
  - parcel-plugin-xxx

  - 无配置(内置配置)
  - 内置依赖, 自动安装缺失依赖
  - HMR

- Loader

  - 以 Babel-Loader 为例, 讲讲 loader 都做了什么
  - 常用的 loader

- Plugin

  - plugin 都做了什么?

  - Webpack 事件流模型 [Tapable](https://github.com/webpack/tapable)

- 性能调优

  - 确定问题
    - bundle-analyzer-plugin
    - speed-measure-plugin

  - 打包速率

    - 分离Dev与Prod配置!

    - 减少查找时间 
      - resolve
        - extension
        - resolve
        - alias
      -  在 loader 中针对性的 exclude 掉无关文件夹, 比如在 url-loader/file-loader 处理图片的配置你就可以把 assets 以外的目录去掉
    - DLL(`Dynamic Link Library`, 动态链接库, 已经不推荐使用)
    - 开启多进程打包(thread-loader)
    - 缓存(babel-loader与terser都有, webpack5默认的是hard-source-plugin)
    - 合理配置source-map

  - 打包大小

    - 擦除JS&CSS死代码

    - JS/CSS 摇树优化(仅在ESM的静态加载下生效) 按需加载
    - 压缩 & Uglify(`Terser`)
    - 代码分割(`Code Spilting`), 讲讲`SplitChunksPlugin`, 讲讲 Dynamic Import

  - chunk hash值 & http缓存配置

  - 打包交互友好度(可选, 但很好玩 hhh)

    - 进度指示(`webpackbar`)
    - 错误友好提示(`friendly-errors-plugin`)

