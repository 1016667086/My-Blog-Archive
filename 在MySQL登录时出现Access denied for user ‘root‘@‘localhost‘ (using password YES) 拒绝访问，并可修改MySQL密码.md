* ## 适用于windows安装MySQL
* ### 对于出现拒绝访问root用户的解决方案

错误1045（28000）：用户'root'@'localhost'（使用密码：YES）拒绝访问

![](https://i-blog.csdnimg.cn/blog_migrate/841ad505d4c35ad723007c0e9a47ca86.png)

首先解析此英文：ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)；解析的地方有两处：①Access denied（拒绝访问）；②using password：NO/YES

![](https://i-blog.csdnimg.cn/blog_migrate/1fed1508bfb6655219abe75a3ba7eebf.png)

一、出现access denied的原因有如下可能：

   1）mysql的服务器停止

   2）用户的端口号或者IP导致

   3）mysql的配置文件错误----my.ini等文件

   4）root用户的密码错误

1. 若MySQL已经没有启动，重启MySQL服务器：**net start mysql**
2. 若用户的端口号与IP（3306/3307）不一致，打开my.ini文件进行编辑。**全部将端口编辑替换为： port=X（如：port=3306）**
3. my.ini文件误输入无效内容，不知道到何处。复制替换该文件；有人已经对my.ini文件进行解释以及注释（非博主的文章）<https://blog.csdn.net/lienfeng6/article/details/78140404>
4. root用户密码错误，本博文章主要内容**【解决方案】**

出现 using password的原因如下是：

1. 不键入密码：![](https://i-blog.csdnimg.cn/blog_migrate/2b88f3e5b7e2336b58b8664fb9221790.png)
2. 错误的密码：![](https://i-blog.csdnimg.cn/blog_migrate/8278ddd8afe705bbf8ccb1ba5694a54d.png)

* ### 解决方案：

到安装的MySQL的目录下，找my.ini文件；

![](https://i-blog.csdnimg.cn/blog_migrate/0a25a11359d5467a98f47864ba7af96f.png)

在[mysqld]后添加skip-grant-tables（使用 set password for设置密码无效，且此后登录无需键入密码）

skip-grant-tables     #在my.ini，[mysqld]下添加一行，使其登录时跳过权限检查

![](https://i-blog.csdnimg.cn/blog_migrate/9adde8529f3f36a1362b0aaaf36a1dd0.png)

**尽量少操作**

重启MySQL服务器。

![](https://i-blog.csdnimg.cn/blog_migrate/54d4f1ba8a17fad5e25974d1eb1ccbd0.png)

登录mysql，键入mysql –uroot –p；直接回车（Enter）

![](https://i-blog.csdnimg.cn/blog_migrate/31c09d9093b8439d300afe334c4f4309.png)

键入无效set password for ‘root’@‘localhost’=password(‘123456’);

![](https://i-blog.csdnimg.cn/blog_migrate/de5d2a8bc41481b6f25282a34c7d38bd.png)

在my.ini文件添加从此后无需键入密码

再把my.ini的skip-grant-tables删除，然后重启MySQL服务器：***net stop mysql ;net start mysql;***

再次进行设置密码：set password for ‘root’@‘localhost’=password(‘123456’);

![](https://i-blog.csdnimg.cn/blog_migrate/6c25ca2e11fb936c69ea190d07e973c4.png)

设置密码成功。。。

skip-name-resolv        #禁止MySQL对外部连接进行DNS解析，使用这一选项可以消除MySQL进行DNS解析的时候。但是需要注意的是，如果开启该选项，则所有远程主机连接授权都要使用IP地址方式了，否则MySQL将无法正常处理连接请求！