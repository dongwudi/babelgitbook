# @babel/core

Babel 的核心功能包含在 @babel/core 模块中。通过以下命令安装：

```
npm install --save-dev @babel/core
```

可以通过`npx babel --help`查看相应的命令参数。  
此时如果在命令行中运行命令：

```
npx babel ./src/ --out-dir lib
```

发现代码并没有什么改变，这时就需要我们安装插件或预设来配合babel的转译。

