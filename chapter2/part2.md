# @babel/preset-env
@babel/preset-env是一个聪明的预设，它允许您使用最新的JavaScript不需要干涉在你的目标环境中语法转换。
```
npm install --save-dev @babel/preset-env
```
安装成功后在`.babelrc`中进行配置：
```
{
  "presets": [
    "@babel/preset-env"
  ],
  "plugins": []
}
```
再次运行`npx babel ./src/ --out-dir lib/`便成功的进行的babel编译。

