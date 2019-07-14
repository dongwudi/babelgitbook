# @babel/polyfill

Babel 几乎可以编译所有时新的 JavaScript 语法，但对于 APIs 来说却并非如此。不是所有的 JavaScript 环境都支持新的api。polyfill 即是在当前运行环境中用来复制（意指模拟性的复制，而不是拷贝）尚不存在的原生 api 的代码。
Babel 用了优秀的 core-js 用作 polyfill，并且还有定制化的 regenerator 来让 generators（生成器）和 async functions（异步函数）正常工作。
如何安装呢？
```
npm install --save @babel/polyfill
```
然后只需要在文件顶部导入即可：
```
import "babel-polyfill";
```
如果配合webpack使用，用多种方式来包含polyfill：
1. 当使用`@babel/preset-env`时：
```
{
  "presets": [
    [
      "@babel/preset-env",
      {
        "useBuiltIns": "entry"
      }
    ]
  ]
}
```
* 在.babelrc中配置`useBuiltIns: 'usage'`,在`webpack.config.js`中的入口数组中没有包含`@babel/polyfill`。`@babel/polyfill`依然会被导入。
* 在.babelrc中配置`useBuiltIns: 'entry'`,在入口文件中使用`require`或者`import`引入。
* 在.babelrc中配置`useBuiltIns: false'`,在`webpack.config.js`中的入口数组中包含`@babel/polyfill`
```
entry: ["@babel/polyfill", "./app/js"]
```


