## 实验六 Linux网络管理

### 一、实验目的

熟悉Linux网络管理基本命令；探索Linux服务器应用。

### 二、实验内容

#### 1.常用网络命令使用。

#### 2.搭建Linux下的FTP服务器。

## 三、主要实验步骤

1.查看操作系统的代码核心版本和发行版本，利用ping命令往任意知名网站发送7次数据包测试网络连通性，利用hostname、ip或其他命令查看系统的IP地址。

#### 一、准备工作：查看系统信息与网络配置

查看系统版本与内核版本  
bash

## 查看 Ubuntu 发行版本（图形化/文本界面通用）

lsb\_release -a

## 或查看内核版本

uname -r

## 或查看完整系统信息（含内核）

cat /proc/version

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b6d25af9978342d5b748374d75ca952c.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0c81dbc079294fc2bb6cc33fcb314c29.png)

```
查看 IP 地址
bash

```

## 推荐使用新工具（现代 Ubuntu 通用）

ip addr show

## 或简化命令

```
hostname -I

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0b26266d365b4d17823fb9e6dfa57ad6.png)

```
测试网络连通性
bash
ping -c 7 www.baidu.com  # 发送 7 次数据包

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7882b2a6845641499af95a37694ab6ac.png)

2.（下边步骤涉及到大量教材没有讲到的领域，可以在deep seek等AI工具辅助下完成实验）查看系统服务，是否安装了ftp服务器软件，如果没有，则首先安装VSFTPD，安装成功后，开启系统FTP服务，并设置FTP服务开机自动启动。使用系统用户账号登录（如ftp用户或普通用户）FTP服务器，检查是否成功连接并访问FTP目录。

```
检查是否安装 VSFTPD
bash
dpkg -l | grep vsftpd  # 若未安装，无输出

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e49d813821e642fe8cb4ab4cb9057e25.png)

```
安装 VSFTPD（需管理员权限）
bash
sudo apt-get update
sudo apt-get install vsftpd -y

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/db4b39e3891041c1b624129f0289216c.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5589f294d00444e0b2a98e3fc3b9863e.png)

```
启动服务并设置开机自启
bash
sudo systemctl start vsftpd       # 启动服务
sudo systemctl enable vsftpd      # 设置开机自启
sudo systemctl status vsftpd     # 检查服务状态（确保 active(running

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6b4b90c9812a4cf1b17590950559a4eb.png)

3.配置FTP服务器，在Ubuntu系统下通常是/etc/vsftpd.conf。设置禁止匿名登录、允许本地用户登录、禁止用户访问其他目录（限制在主目录）等。

## 三、创建 FTP 专用用户 lhn

创建用户并指定主目录  
bash  
sudo useradd -d /home/lhn -m -s /bin/bash lhn # -m 创建主目录，-s 指定默认 shell

```
设置用户密码
bash
sudo passwd lhn  # 输入两次密码（例如：密码设为 `lhn123`）

创建 FTP 文件存储目录并设置权限
bash
mkdir -p /home/lhn/ftp  # 在用户主目录下创建 ftp 目录
chown -R lhn:lhn /home/lhn/ftp  # 设置目录所有者为 lhn
chmod 755 /home/lhn/ftp  # 赋予目录读取和执行权限（禁止匿名写入）

```

4.创建一个专门的FTP账户zhangsanftp（方法同实验四），设置好密码，创建FTP文件存储目录，设置目录权限为仅允许用户访问。重启FTP服务，使上述设置生效。

## 四、配置 VSFTPD 服务器

备份原始配置文件  
bash  
sudo cp /etc/vsftpd.conf /etc/vsftpd.conf.bak

编辑配置文件（禁止匿名登录，限制本地用户）  
bash  
sudo nano /etc/vsftpd.conf # 或使用 vi/vim

修改以下参数（删除注释或直接添加）：

```
conf
anonymous_enable=NO         # 禁止匿名登录
local_enable=YES            # 允许本地用户登录
write_enable=YES            # 允许用户写入（上传文件）
local_umask=022             # 文件创建权限（默认 077-022=055，目录 077-022=055）
chroot_local_user=YES       # 限制用户在主目录（禁止访问其他目录）
userlist_enable=YES         # 启用用户列表
userlist_file=/etc/vsftpd.user_list  # 用户列表文件（默认存在）
userlist_deny=NO            # 用户列表中的用户允许登录（与匿名相反）

```

保存并退出（nano 按 Ctrl+O，vi 按 :wq）。  
重启 FTP 服务使配置生效  
bash

```
sudo systemctl restart vsftpd

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9473e54a0cbd42e08d67348006a0dcf6.png)

5.将/usr/share/dict目录下的文件复制到FTP目录，作为测试文件。这里也可网上下载或自己生成若干测试目录和文件。

```
准备测试文件

复制系统字典文件到 FTP 目录（作为测试文件）
bash
cp -r /usr/share/dict/* /home/lhnftp/ftp/  # 复制所有字典文件


验证文件是否存在
bash
ls -l /home/lhnftp/ftp  # 应显示复制的文件（如 `american-english` 等）

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f1cfd9c64cbd4815acc3ab706278b0b4.png)

6.在命令行利用FTP命令或者利用客户端软件访问FTP服务器，测试匿名账号、专用账号zhangsanftp的上传、下载功能是否运行正常。  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8abb439652c04481a1de4c281b2a94f4.png)

测试 FTP 服务器连接  
使用命令行工具 ftp 登录（本地测试）  
bash  
ftp localhost # 或使用服务器 IP（如 192.168.1.100）

## 登录时输入用户名 `lhnftp` 和密码 `lhnftp123`

```
ftp> ls         # 查看 FTP 目录文件（应显示字典文件）
ftp> get american-english  # 下载文件到本地
ftp> put test.txt  # 上传本地文件（需先创建 test.txt）
ftp> quit        # 退出

```

> 使用图形化客户端（如 finalshell） 主机：输入虚拟机 IP（如 192.168.1.100） 协议：FTP - 文件传输协议  
> 登录类型：正常 用户名：lhnftp，密码：lhnftp123 连接后验证文件上传 / 下载功能。
>
> 根据你给出的错误信息 500 OOPS: vsftpd: refusing to run with writable root inside  
> chroot()，这表明 VSFTPD 不允许用户在被 chroot 限制的主目录下有写入权限。chroot  
> 是一种安全机制，它会将用户的活动范围限制在指定的目录内，而 VSFTPD  
> 为了保证安全，默认不允许用户的主目录具有写入权限。下面为你提供解决办法：
>
> 1. 创建一个不可写的根目录 在用户的主目录下创建一个不可写的根目录，并且将用户的文件存放在该目录下。 bash

## 以 lhnftp 用户为例，创建一个新的目录作为 FTP 根目录

```
sudo mkdir -p /home/lhnftp/ftp
sudo chown lhnftp:lhnftp /home/lhnftp/ftp
sudo chmod 555 /home/lhnftp/ftp

```

## 在 ftp 目录下创建一个可写的子目录用于文件上传和下载

```
sudo mkdir -p /home/lhnftp/ftp/files
sudo chown lhnftp:lhnftp /home/lhnftp/ftp/files
sudo chmod 755 /home/lhnftp/ftp/files

```

2. 修改 VSFTPD 配置文件  
   编辑 /etc/vsftpd.conf 文件，确保 chroot\_local\_user=YES 并且用户的主目录指向新创建的不可写根目录。  
   bash  
   sudo nano /etc/vsftpd.conf  
   找到 chroot\_local\_user 和 local\_root 配置项，如果没有则添加，修改后的内容如下：  
   plaintext  
   chroot\_local\_user=YES  
   local\_root=/home/lhnftp/ftp
3. 重启 VSFTPD 服务  
   修改配置文件之后，需要重启 VSFTPD 服务使配置生效。  
   bash  
   sudo systemctl restart vsftpd
4. 再次测试登录  
   完成上述步骤后，再次尝试使用 lhnftp 用户登录 FTP 服务器。  
   bash  
   ftp 127.0.0.1  
   当提示输入用户名和密码时，分别输入 lhnftp 和对应的密码，然后尝试进行文件的上传和下载操作。  
   通过以上步骤，应该可以解决 500 OOPS: vsftpd: refusing to run with writable root inside chroot() 错误，让你能够正常登录并使用 FTP 服务。

7.设置开启匿名帐号访问FTP，设置好匿名帐号访问指定的目录，重启FTP服务使设置生效，测试匿名账号使用效果。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1855870244a14141b68ac5433464dfdf.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c244fbde5b024bdfa210502e997104c9.png)

## 作业四

从计算机网络的角度，简述下FTP协议的工作原理和潜在问题。随着网络技术的发展，FTP协议逐渐暴露出一些不足之处。请列举至少两种FTP协议的替代方案，并比较它们与FTP协议的优缺点。

> 答： FTP协议原理与潜在问题 FTP基于客户端 -  
> 服务器模型，通过控制连接（端口21）传输命令，数据连接传输文件，有主动和被动模式。但它存在明显不足，采用明文传输，易被窃听，在防火墙环境下兼容性差，且处理大文件或多小文件时效率低。
>
> 替代方案及对比  
> -SFTP基于SSH加密，安全性高、防火墙友好且支持断点续传，但传输稍慢。
>
> * HTTP/HTTPS广泛支持，HTTPS安全，性能有优化，不过文件管理功能弱。与FTP相比，它们在安全和性能上有优势，能更好适应现代网络需求。