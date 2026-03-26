## 问题描述：

虚拟机运行Linux命令，下载Redis时，报如下错误：  
wget: unable to resolve host address “download.redis.io”  
Resolving download.redis.io… failed: Temporary failure in name resolution.  
wget: unable to resolve host address “download.redis.io”

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/7a1e99ad7b5db42db5678806df0ad723.png#pic_center)

---

## 解决方案：

`vim /etc/resolv.conf` 打开配置文件。  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/630140543271e8c51b0cdc64c9e54f9f.png#pic_center)

在nameserver 下增加两句，然后**Esc**键，再 **:wq** 结束保存退出。

```
nameserver 8.8.8.8
nameserver 8.8.4.4

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/ef33e9ad1a23a9ae8fc7977075b3a9f3.png#pic_center)

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/b0992b51e3e828b548ab6d1fbaf93d5f.png#pic_center)  
**之后再执行，$ wget http://download.redis.io/releases/redis-5.0.5.tar.gz。**

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/0becd201283b1e60ff9c535f5417a413.png#pic_center)

完美下载redis-5.0.5。