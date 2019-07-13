从版本 7 开始所需要的所有的Babel模块都是@babel 作为冠名的。

# @babel/cli

@babel/cli 是一个能够从终端（命令行）使用的工具。适合本地安装。下面是其安装命令和基本用法：

```
npm install --save-dev @babel/cli
```

然而我在命令行查看babel版本时，出现了缺少`@babel/core`的提示：

```
$ npx babel -v
Cannot find module '@babel/core'
```

`npx`会调用项目内部安装的模块。

@babel/cli是依赖一个叫@babel/core的包文件。

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

