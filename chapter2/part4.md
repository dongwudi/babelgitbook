Babel 使用了非常小的 helpers 来实现诸如 _extend 等常用功能。默认情况下，它将被添加到每个通过 require 引用它的文件中。这种重复（操作）有时是不必要的，特别是当你的应用程序被拆分为多个文件时。
这时则需要使用@babel/plugin-transform-runtime：所有的 helper 都会引用模块 babel-runtime，以避免编译输出的重复问题。这个运行时会被编译到你的构建版本当中。
# 安装
在大多数情况下，你应该安装@babel/plugin-transform-runtime作为开发依赖（使用 --save-dev）
```
npm install --save-dev @babel/plugin-transform-runtime
```
将@babel/runtime作为生产依赖（使用 --save）
```
npm install --save @babel/runtime
```
# 使用
```
{
  "plugins": ["@babel/plugin-transform-runtime"]
}
```