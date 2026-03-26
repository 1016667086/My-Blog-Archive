* 前言  
   目前网上关于vue-cli的文字/视频教程多数停留在2.9.6或3.x版本，但毕竟IT行业学新的总不会错。官方推出的版本从3.0开始也做了较大的变动，这里简单做个升级教程。

**- 卸载旧版本**  
 卸载命令：`npm uninstall -g vue-cli`  
 这里有坑，如果明明卸载了却仍出现报错类似提示没有卸载干净，可能是当时安装旧版本时你还使用了yarn导致有残留，用yarn uninstall -g vue-cli清理干净。

**- 安装最新版**  
 自3.0版本后，官方声明这个工具改名为@vue/cli。  
 安装命令：`npm install -g @vue/cli` 或 `yarn install -g @vue/cli`

**- 检查新版本**  
 打开终端输入命令行：`vue -V`（是大写V，不是小写）  
 如下显示 @vue/cli 4.1.2 说明安装成功。  
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/25ab016065b71e31881e2b15f4b22e9f.png)  
 vuecli新版本创建项目教程见我下一篇…