# npm-hello

## 简介
第一个npm 模块

## 调试
[参考：《你所不知道的模块调试技巧 - npm link》=](https://github.com/atian25/blog/issues/17)

1. `npm link #先去到模块目录，把它 link 到全局（在node安装目录node_modules中生成一个link，本地是C:\Program Files\nodejs\node_modules）`
2. `npm link npm-hello # 再去项目目录通过包名来 link (name必须是 package.json中name)`
3. `npm unlink npm-hello #项目目录卸载`