# Webpack & Parcel

> Parcel 是可选的

- compiler 与 compilation, Webpack 构建流程

- HMR(`Hot Module Reloading`)原理

- Webpack 构建流程
- Parcel 构建流程

  - @parcel/transformer-xxx
  - parcel-plugin-xxx

- Loader

  - 以 Babel-Loader 为例, 讲讲 loader 都做了什么
  - 常用的 loader

- Plugin

  - plugin 都做了什么?

  - Webpack 事件流模型 [Tapable](https://github.com/webpack/tapable)

- 性能调优

  - 打包速率

    - 减少查找时间 -> 在 loader 中针对性的 exclude 掉无关文件夹, 比如在 url-loader/file-loader 处理图片的配置你就可以把 assets 以外的目录去掉, 蚊子腿再小也是肉!
    - DLL(`Dynamic Link Library`, 动态链接库, 已经不推荐使用)

    - 开启多进程打包
    - 影响编译速度的配置(如`source-map`)
    - hardsource-webpack-plugin

  - 打包大小

    - JS/CSS 摇树优化 按需加载
    - 压缩 & Uglify(`Terser`)
    - 代码分割(`Code Spilting`), 讲讲`SplitChunksPlugin`, 讲讲 Dynamic Import

  - 打包交互友好度(可选, 但很好玩 hhh)

    - 进度指示(`webpackbar`)
    - 错误友好提示(`friendly-errors-plugin`)
