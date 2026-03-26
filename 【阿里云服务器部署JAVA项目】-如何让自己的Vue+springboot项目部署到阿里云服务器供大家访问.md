购买服务器（试用白嫖）

![](https://i-blog.csdnimg.cn/blog_migrate/d6b4e0a4d8ed90ef08bd309113ef3f9c.png)

![](https://i-blog.csdnimg.cn/blog_migrate/3fdc1152f012e56b24764368b552e4f7.png)

#### 2.购买域名

[官网](https://cn.aliyun.com/ "官网")

域名的作用的是为了[DNS解析](https://so.csdn.net/so/search?q=DNS%E8%A7%A3%E6%9E%90&spm=1001.2101.3001.7020 "DNS解析")，这样被人访问的不再是一连串的IP地址，而是形如 **www.xxx.com** 这样的网站

![](https://i-blog.csdnimg.cn/blog_migrate/6b803a36432a870e90799165e2c1ffe9.png)

[域名购买](https://so.csdn.net/so/search?q=%E5%9F%9F%E5%90%8D%E8%B4%AD%E4%B9%B0&spm=1001.2101.3001.7020)流程较长，还需备案，所以能提前准备好，10块左右买个.top域名

![](https://i-blog.csdnimg.cn/blog_migrate/226e877e865043bab063cda1318c4ee0.png)

2.1 添加域名解析

![](https://i-blog.csdnimg.cn/blog_migrate/bee83f29852652eaa668368a2388c13c.png)

 添加解析两个地址![](https://i-blog.csdnimg.cn/blog_migrate/db915d0227e9a4723f570035ca39d44b.png)

##### 2.2 将域名ICP备案一下

 云服务选择ECS服务器，可以自动绑定IP进行备案![](https://i-blog.csdnimg.cn/blog_migrate/7e1e4ee07841063abca3575e636979a2.png)

 （可以提前实名认证IP加快进度）

#### 3.远程连接使用宝塔配置

##### 3.1远程连接登录到云服务器

阿里云服务器支持多种远程连接方式，可以使用阿里云自带的[Workbench远程连接](https://help.aliyun.com/document_detail/71529.html?source=5176.11533457&userCode=r3yteowb "Workbench远程连接")方式，也可以使用第三方SSH远程连接软件如PuTTY、Xshell等。阿里云服务器网使用阿里云自带的远程连接方式：

首先登录到云服务器ECS管理控制台，左侧栏【实例与镜像】>>【实例】，找到目标云服务器ECS实例，然后点击右侧的【远程连接】，如下图：

![](https://i-blog.csdnimg.cn/blog_migrate/039ee4c2b785385c089d1fa49e9af404.png)

###### **3.2重置下密码**

###### 3.3执行宝塔面板的安装命令

登录到你的云服务器后，执行宝塔面板安装命令，阿里云服务器网使用的CentOS操作系统，命令如下：

```
yum install -y wget && wget -O install.sh https://download.bt.cn/install/install_6.0.sh && sh install.sh ed8484bec代码解读
```

其他操作系统安装宝塔面板脚本，请移步到：阿里云服务器安装宝塔Linux面板命令脚本大全

执行宝塔Linux面板安装命令后，会提示如下：

```
Do you want to install Bt-Panel to the /www directory now?(y/n): y代码解读
```

保持默认，回复个字母“y”，如下图：

![](https://i-blog.csdnimg.cn/blog_migrate/3a45b0ce79279cafd4ffb01f4ca33b0e.png)

然后回车，系统会自动安装，大约1分钟左右会自动安装完成。

###### 3.4 宝塔面板登录地址、账号和密码

宝塔面板自动安装完成后，会显示宝塔后台登录地址、username和password，如下图：

![](https://i-blog.csdnimg.cn/blog_migrate/0a0a835189d05277882b1fb3abe4e412.png)

如上图所示，保存好上述信息，后续登录到宝塔面板后台的时候会用到。如果是通过外网登录宝塔后台，就是用外网面板地址，如果是在云服务器上登录宝塔可以使用内网面板地址。

###### 3.5 在阿里云服务器控制台开通宝塔面板端口

最初宝塔面板的端口号是8888，出于安全考虑，现在宝塔面板使用的端口是程序安装完成后随机生成的端口号，在步骤四图中的面板地址中可以看出，端口号为39118，注意：这个端口号是随机生成，你的宝塔面板端口号可能不是这个。在云服务器ECS的[安全组](https://help.aliyun.com/document_detail/25471.html?source=5176.11533457&userCode=r3yteowb "安全组")中开启宝塔端口号。

1、登录到ECS云服务器管理控制台

2、左侧栏找到【实例与镜像】>>【实例】，找到目标ECS实例，点击实例ID进入到实例详情页

3、切换到【安全组】页面，点击右侧【配置规则】，如下图：

![](https://i-blog.csdnimg.cn/blog_migrate/bbc26fe8bfb6027c1f5fa508b4a704e6.png)

4、在入方向点击【手动添加】，端口范围填写宝塔面板端口号，授权对象选择【0.0.0.0/0】，如下图：

![80duankou.jpg](https://i-blog.csdnimg.cn/blog_migrate/1da97f9aee52a0ebd164c4a6d7d7b55f.jpeg)

 我这里选择放行全部

![](https://i-blog.csdnimg.cn/blog_migrate/9b34c73f2fc2da8b6fe5dd18d327731e.png)

![](https://i-blog.csdnimg.cn/blog_migrate/11a3f2911c9c99cd6d8c5cfb083bb067.png)

安全组规则设置完后，然后点【保存】即可，不需要重启云服务器，安全组规则保存后立即生效，宝塔面板端口号就已经开通了。

关于阿里云安全组开通端口详细教程参考下方文档：

> 详细教程参考：
> [https://help.aliyun.com/document\_detail/25471.html](https://help.aliyun.com/document_detail/25471.html?source=5176.11533457&userCode=r3yteowb "https://help.aliyun.com/document_detail/25471.html")

###### 3.6 登录到宝塔管理地址并安装LNMP环境

在浏览器中粘贴宝塔面板的外网面板地址，并输入账号和密码，登录到宝塔面板管理后台，第一次登录需要勾选同意协议，然后进入面板。然后绑定宝塔帐号，有宝塔账号的话，直接输入手机号和密码登录即可。没有宝塔账号的话，就点免费注册一个宝塔账号。

然后会弹出推荐安装套件窗口，如果是搭建Web网站应用，可以选择LNMP(推荐)，点击【一键安装】，如下图：![](https://i-blog.csdnimg.cn/blog_migrate/8a404abf566ff18814f25010147eb884.png)

会弹出消息盒子，显示安装进度。也可以根据自身实际需求，选择所需的环境进行安装，在宝塔面板后台的【软件商店】中可以选择安装运行环境，还可以安装一些其他应用等，如下图：

![yunxinghuanjing.jpg](https://i-blog.csdnimg.cn/blog_migrate/1e7452d018459651a41e76d1dcfb6730.jpeg)

更多关于阿里云服务器使用说明，请以官方页面为准：[https://www.aliyun.com/product/ecs](https://www.aliyun.com/product/ecs?source=5176.11533457&userCode=r3yteowb "https://www.aliyun.com/product/ecs")

#### 4.宝塔数据库相关

###### 4.1安装mysql

![](https://i-blog.csdnimg.cn/blog_migrate/030359d7fb5d418ec9b8b7107aa5be80.png)

然后我们在宝塔面板安全页面开放一个3306的端口

![](https://i-blog.csdnimg.cn/blog_migrate/f50f46e81fdcc9f0f9976568d0559887.png)

导入数据库文件

###### 4.2安装redis

![](https://i-blog.csdnimg.cn/blog_migrate/bee2659e166d03428c23d9f2baca45c1.png)

直接下载 配置redis相关配置文件

端口从127.0.0.1修改为0.0.0.0

![](https://i-blog.csdnimg.cn/blog_migrate/576973e945c7611c464ab443d1861b55.png)

放开6379端口

![](https://i-blog.csdnimg.cn/blog_migrate/686ca6b7bdbbc9a23fdf912ed3293b87.png)

> **配置完重启一下，确保配置生效**

#### 5.环境配置上线

###### 5.1安装jdk和tomcat

Spring boot 项目只需要JDK 环境即可部署成功

而内置项目和独立项目是需要安装Tomcat 才能进行部署

tomcat 的安装目录和端口如下：  
 tomcat7   安装目录 /usr/local/bttomcat/tomcat7    端口号8231  
 tomcat8   安装目录 /usr/local/bttomcat/tomcat8    端口号8232

tomcat9   安装目录 /usr/local/bttomcat/tomcat9    端口号8233

【注意：Ubuntu/Debian 不支持tomcat7， 如需安装tomcat7 可使用CentOS7等系列】

(安装tomcat时会自动装上JDK，我这里安装的是tomcat7)

![](https://i-blog.csdnimg.cn/blog_migrate/183a2781eb6544a5b07a66bcc52cf6ab.png)

②安装完成后，我们可到服务器终端执行以下命令来验证Java环境是否已成功安装

```
/usr/local/btjdk/jdk8/bin/java -version代码解读
```

1. 如果输出了Java版本信息，则说明Java环境已经安装成功。

###### 5.2 将后端打包上传

![](https://i-blog.csdnimg.cn/blog_migrate/4760aca2b5c4127dc1307bc077955fa4.png)

 将jar包上传到宝塔

![](https://i-blog.csdnimg.cn/blog_migrate/c2725d55006a45a5061b1a7ffc37a7ee.png)

将项目提交部署

###### 5.3 将前端打包上传

1. Vue项目执行打包命令进行打包得到dist文件夹

```
npm run build代码解读
```

2.将dist文件夹上传到宝塔

3.php项目页面新增站点![](https://i-blog.csdnimg.cn/blog_migrate/b1d6d416ae2840585a578a4a7505f67e.png)

如果运行接口异常的话记得改一下权限

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/713aba6be11e4af8bcbdc9d70217de86.png)

![](https://i-blog.csdnimg.cn/blog_migrate/8763bdba7ff79bcd31be431ef3980694.png)

**配置好就可以用地址去访问了**

最后重启一下nginx即可

## 如果部署成功后刷新碰到404请配置nginx的配置文件重定向问题

在配置文件中加上

```
 try_files $uri $uri/ /index.html;



```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6526e0937b4445f0a9d9739690da2336.png)