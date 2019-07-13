# .babelrc
在你的项目中创建名为 .babelrc 的文件，并输入以下内容。
```
{
  "presets": [],
  "plugins": []
}
```
也可以在package.json中将.babelrc的配置信息作为babel 键（key）的值添加到 package.json 文件中：
```
{
  "name": "babel",
  "version": "1.0.0",
  "babel": {
    "presets": [],
    "plugins": []
  }
}
```
