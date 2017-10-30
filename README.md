# npm-hello

## 简介
第一个npm 模块

## 调试
[参考：《你所不知道的模块调试技巧 - npm link》=](https://github.com/atian25/blog/issues/17)

1. `npm link #先去到模块目录，把它 link 到全局（在node安装目录node_modules中生成一个link，本地是C:\Program Files\nodejs\node_modules）`
2. `npm link npm-hello # 再去项目目录通过包名来 link (name必须是 package.json中name)`
3. `npm unlink npm-hello #项目目录卸载`


## 国内环境问题
1. npm 使用 nrm 来配置，设置代理 [npm配置镜像、设置代理](https://segmentfault.com/a/1190000002589144)
2. 常用命令
   ` nrm ls #列表`
   ` nrm use taobao #切换`
   ` nrm test  #测速`


## 具体原理
1. `npm link` 具体实现
    在目录 `C:\Users\caoyi\AppData\Roaming\npm` 下创建 ‘[项目名].cmd’;

    ‘[项目名].cmd’主要是引用到`package.json`文件中`bin`命令

    并在`C:\Users\caoyi\AppData\Roaming\npm\node_modules`下创建软链接，链接到具体项目目录底下