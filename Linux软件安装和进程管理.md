## 实验五 Linux软件安装和进程管理

### 一、实验目的

熟悉Linux软件包管理；熟悉Linux进程管理。

### 二、实验内容

1.软件包更新。  
2.软件安装和卸载。  
3.Linux系统信息查看。  
4.Linux进程管理。

### 三、主要实验步骤

1.Ubuntu系统下，查看系统已安装的软件包，更新本地的软件包索引数据库。利用apt相关工具安装新软件，比如tldr、codeblocks、RabbitVCS、finger、sl、at等等。注意软件安装需要用到root权限。

查看已安装软件包

```
dpkg -l # 或 apt list --installed

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e72a1a99a43e4861b6aaffac2ecb4b9e.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/22318939938e420da687b28abc8aef0e.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3c74e7f548c54e1f81ce32256fddc974.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/db3a89ce68fc4bb4bab90f53d1f30fd9.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5a2c39973d45407081f8695f187b50e4.png)

**更新软件包索引**

```
sudo apt update

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bfbdc6be6cae4346948070c47cac28db.png)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9e1cef8edf3c4350bed10a5fbadd1c67.png)

安装指定软件（任选 3 个以上）

```
sudo apt install tldr codeblocks rabbitvcs finger sl at

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4e18515c7e6e4a1f9c18419ce32d46a4.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ca4a8375c9ac4df589371cc8672f1094.png)

2.利用tldr学习tar命令的用法，将/usr/share/下的目录dict及其内容打包成主目录下的zhangsan.tar，利用gzip或其他压缩工具将zhangsan.tar压缩成新文件，最后查看下tar包和压缩文件的大小。

**`学习 tar 命令`**

发下并没有tldr命令： 通过 sudo snap install tldr 和sudo apt install tldr -hs 命令安装tldr解压压缩命令。  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/42ce7e54d7dc4a20903693b93212a7fa.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/022676707ccf46788d3fcbe36208c0c9.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0308641cf05547c5b3dde1c900820f97.png)  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/55732856bad645768e0182f3cbe9c1d2.png)

发现tldr 安装成功， 但是显示错误，未连接，失败。  
打包目录

```
tar -cvf ~/zhangsan.tar /usr/share/dict

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/403c909064f240929c68f11fd9a00872.png)

压缩打包文件  
gzip ~/zhangsan.tar  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0e84ee84a03648198f690f08dec58b6a.png)

```
# 或使用bzip2 bzip2 ~/zhangsan.tar

```

查看文件大小

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a675b9a41bc54c6f9f426149855afc97.png)

```
ls -lh ~/zhangsan*

```

3.利用uname分别查看Linux系统内核版本和发行版本信息，利用uptime分别查看系统启动时间和运行时间。（对于不熟悉的命令，多查下用户手册或tldr，下同）

系统信息查看

查看内核版本  
uname -r  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cb1138105c1b4c20a1a2dba546570899.png)

继续查看发行版本：lsb\_release -a

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/074818b0b4be4d84a00c551dab0f966e.png)

查看系统运行时间：uptime

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f424ba9172844a67917275d865f63543.png)  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4e169260c77c48da846f89d4a19133c1.png)

4.利用ps查看所有运行的进程，利用top查看本用户所拥有的进程的动态变化，利用free以human-readable方式查看内存使用情况。

进程管理操作

查看所有进程：

ps aux

```
# 或 ps -e

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5d029afb20d9414bbcb70db34a3157f3.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c9a6ef2f104c489cb735f4abf29dd406.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/926fe8b917c24597b5acc58523c06700.png)

动态查看进程  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4c7783e280d7494bbcf106513fd2f4b2.png)  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c89943815d844ea19df024f1a12729a1.png)

查看内存使用：free -h  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f8d5a8dbdc3f4b1083f43f3bb89066c3.png)

```
可以看出total        used        free      shared  buff/cache   available
内存：         3.8Gi       1.4Gi       132Mi        37Mi       2.5Gi       2.3Gi
 总共3.8个G，  使用快乐1.4G  还剩下可用内存2.5个G

```

5.通过后台执行xlogo命令，通过后台执行sleep 300命令，时间大于十分钟。

后台任务管理：启动后台任务  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7f124dba72f34a138cf6ae3454954564.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9f86eb5ce9fb443eaf1b8ee414326315.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fa65621106604cc7ba1b24476a634e41.png)

暂停并后台执行

sleep 600

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6e64fead9f914e3caab51d0b5eb945d1.png)

```
# 按Ctrl+Z暂停

```

> bg %1

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9cd36c334dab4466af20f23d44664f8d.png)

6.执行sleep 600，在时间结束前将该任务暂停丢至后台执行。  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8865e6e49a7346028f065ffe2c761373.png)

7.查看所有后台作业的名称、状态、作业号和进程号。在后台将之前暂停的sleep 600开启后台运行，将xlogo拿到前台运行，利用kill相关命令结束xlogo运行。

查看作业列表  
jobs -l  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/70cea6a74a874c2588464e7d41fb3f78.png)

恢复后台任务  
bg %1

前台运行任务

fg %1  
![# 按Ctrl+C终止](https://i-blog.csdnimg.cn/direct/68faae012d944181b9ec1b7cd6b1c578.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9de622e3866540b5af654ff99bf0d065.png)

终止进程 killall xlogo  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8652e46dbae342b6baca9aac44df7812.png)

killall xlogo

## 或使用进程ID

kill

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/afece57943044999b8bf0f98bcb80651.png)