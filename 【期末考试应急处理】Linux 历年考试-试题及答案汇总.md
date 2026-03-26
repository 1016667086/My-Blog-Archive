一、单选  
1 . 存放用户帐号的文件是（C）。  
A. shadow B. group **C. passwd** D. gshadow

2 . 下面哪个系统目录中包含 Linux 使用的外部设备（B）。  
A./bin B./dev C./boot D./home

3 . Linux 系统的联机帮助命令是（D）。  
A. tar B. cd C. mkdir D. man

4 . 如何删除一个非空子目录 /tmp (B )。  
A. del /tmp/\* B. rm -rf /tmp C. rm -Ra /tmp/\* D. rm –rf /tmp/\*

5. 更改一个文件权限的命令是（C）。  
   A. change B. attrib C. chmod D. at
6. 如果执行命令 #chmod 746 file.txt，那么该文件的权限是（A）。  
   A. rwxr–rw- B. rw-r–r— C. --xr–rwx D. rwxr–r—
7. 如果您想列出当前目录以及子目录下所有扩展名为―.txt‖的文件，那么您可以使用的命令是（A ）。  
   A. ls \*.txt B. find –name ―.txt‖ C. ls –d .txt D. find .―.txt‖

8 . 怎样显示当前目录（A）。  
**A. pwd** B. cd C. who D. ls

9 . 欲把当前目录下的 file1.txt 复制为 file2.txt，正确的命令是（D）。  
A. copy file1.txt file2.txt B. cp file1.txt | file2.txt  
C. cat file2.txt file1.txt **D. cat file1.txt > file2.txt**

10．为了达到使文件的所有者有读®和写(w)的许可， 而其他用户只能进行只读访问， 在设置文件的许可值 时，应当设为： ( B )。  
A. 566 **B. 644** C. 655 D. 744

11．为了将当前目录下的压缩归档文件 myftp.tar.gz 解压缩， 我们可以使用： ( A )。  
**A. tar -xvzf myftp.tar.gz** B. tar -xvz myftp.tar.gz  
C. tar -vzf myftp.tar.gz D. tar -xvf myftp.tar.gz

12．用来保存用户名、个人目录等资料的文件是（ B ）。  
A. /etc/shadow **B. /etc/passwd** C. /etc/inittab D. /etc/group

13．一个文件的权限是-rw-rw-r–，这个文件所有者的权限是（ C ）。  
A. read-only B. write **C. read-write**

14 ．绝大多数 Linux 分区使用的文件系统类型是( D )。  
A. vfat B. nfs C. swap **D. ext2**  
15．在 Linux 系统中，硬件设备大部分是安装在( B )目录下的。  
A. /mnt **B. /dev** C. /proc D. /swap

16．比较重要的系统配置资料，一般来说大部分位于( A )目录下。  
**A. /etc** B. /boot C. /home D. /usr

17．要改变文件的拥有权，使用命令( B )。  
A. chgrp **B. chown** C. chsh D. chmod

18．在使用 mkdir 命令创建新的目录时，在其父目录不存在时先创建父目录的选项是（ D ）。 A -m B –d C -f **D –p**

19.局域网的网络地址 192.168.1.0/24，局域网络连接其它网络的网关地址是 192.168.1.1 。主机 192.168.1.20 访问 172.16.1.0/24 网络时，其路由设置正确的是(B )。  
A route add –net 192.168.1.0 gw 192.168.1.1 netmask 255.255.255.0 metric 1  
**B route add –net 172.16.1.0 gw 192.168.1.1 netmask 255.255.255.0 metric 1**  
C route add –net 172.16.1.0 gw 172.168.1.1 netmask 255.255.255.0 metric 1  
D route add default 192.168.1.0 netmask 172.168.1.1 metric 1

20.下列提法中，不属于 ifconfig 命令作用范围的是(D )。  
A 配置本地回环地址 B 配置网卡的 IP 地址  
C 激活网络适配器 **D 加载网卡到内核中**

21.下列文件中，包含了主机名到 IP 地址的映射关系的文件是： (B )。  
A /etc/HOSTNAME **B /etc/hosts** C /etc/resolv.conf D /etc/networks

22.当我们与某远程网络连接不上时， 就需要跟踪路由查看， 以便了解在网络的什么位置出现了问题， 满足 该目的的命令是 ( C) 。  
A ping B ifconfig **C traceroute** D netstat

23.用ls –al 命令列出下面的文件列表， (D )文件是符号连接文件。  
A -rw-rw-rw- 2 hel-s users 56 Sep 09 11:05 hello  
B -rwxrwxrwx 2 hel-s users 56 Sep 09 11:05 goodbey  
C drwxr–r-- 1 hel users 1024 Sep 10 08:10 zhang  
**D lrwxr–r-- 1 hel users 2024 Sep 12 08:12 cheng**

24.在给定文件中查找与设定条件相符字符串的命令为： ( A)。  
**A grep** B gzip C find D sort

25.退出交互模式的 shell，应键入(C ) 。  
A B ^q **C exit** D quit

26,将光盘 CD-ROM （hdc）安装到文件系统的/mnt/cdrom 目录下的命令是(C ) 。  
A mount /mnt/cdrom B mount /mnt/cdrom /dev/hdc  
**C mount /dev/hdc /mnt/cdrom** D mount /dev/hdc

1、Redhat 9 所支持的安装方式有（BCD ）。  
A 通过 Telnet 进行网络安装 **B 从本地硬盘驱动器进行安装  
C 通过 NFS 进行网络安装 D 通过 HTTP 进行网络安装**

2、 如果你是 Red Hat Linux 9 系统管理员，Jack 用户忘记了自己的口令，他希望你帮他将口令清空，为了 达到这个目的你可以通过（D）来实现。  
A 删除/etc/shadow 文件中该用户帐户所对应的记录行  
B 编辑/etc/shadow 文件，将该用户帐户所对应记录中的口令节内容删除 B编辑/etc/shadow文件，将该用户帐户所对应记录中的口令节内容删除  
C 删除/etc/passwd 文件中该用户帐户所对应的记录行  
**D 编辑/etc/passwd 文件，将该用户帐户所对应记录中的口令节内容删除**

3、 下列哪几个符号是 Linux 通配符（CD）。  
A # B @ **C \* D ?**

4、在 Red Hat Linux9 中的图形界面的网络配置中，进行网络配置的主要参数包括：（ABCD）。  
A 网络 IP 地址 B 子网掩码 C 网关 D DNS 服务器地址

5、 Linux 的正常关机命令可以是（AC）。  
**A shutdown -h now** B shutdown -r now **C halt** D reboot

6、 Linux 操作系统结构由（ABCD ）组成。  
**A Linux 内核 B Linux Shell C Linux 文件系统  
D Linux 应用程序**

7、Linux 系统的帐号文件由哪些组成(AB ) 。  
**A. /etc/passwd B. /etc/group** C. /etc/shadow D. /etc/inittab

8 ．Linux 的每类用户拥有三种权限，分别是（ ABC ）。

**A. r B. w C. x** D. m

三. 判断。  
1 .**可以使用 kill 命令来结束 Linux 系统下运行的进程。 V**  
2. Linux 系统管理员的权限和普通用户的权限相同。 X  
**3 . RPM 有 5 种基本操作模式： 安装、删除、升级、查询和校验。 V**  
4 . Linux 系统的任何用户都可以设置计算机的名字。 X  
**5 . Linux 操作系统的特性有：开放性、多用户、多任务、良好的用户界面等。 V**

四、填空题  
1 、链接分为：**（符号链接）**和**（硬链接）**。

2、某文件的权限为： **d-rw-\_r–\_r-**，用数值形式表示该权限， 则该八进制数为：**（644**） ，该文件属性是\*\*（目 录文件）\*\*。

3、在 Linux 系统中，以\*\*（文件）\*\*方式访问设备。

4 、前台起动的进程使用（Ctrl+C）终止，Kill 是后台。

5、安装 Linux 系统对硬盘分区时，必须有两种分区类型：**（ext3）**和**（swap）**。

6、内核分为 **（进程管理系统）、 （内存管理系统） 、（I/O 管理系统）** 和\*\*（文件管理系统）\*\*等四个子系 统。

7 、ping 命令用于测试网络的连通性， ping 命令通过\*\*（ICMP）\*\*协议来实现。

8、在使用手工的方法配置网络时，可通过修改\*\*（/etc/）\*\* 文件来改变主机名，若要配置该计算机的域名解 析客户端，需配置 \*\*（/etc/resolv.conf）\*\*文件。

9、管道就是将前一个命令的\*\*（标准输出）作**为后一个命令的**（标准输入）\*\* 。

10、在 Linux 系统中，测试 DNS 服务器是否能够正确解析域名的客户端命令，使用命令\*\*（nslookup）\*\*

11、欲发送 10 个分组报文测试与主机 abc.tuu.edu.cn 的连通性，应使用的命令和参数是：**（ping abc.tuu.edu.cn –c 10）**

12、在超级用户下显示 Linux 系统中正在运行的全部进程，应使用的命令及参数是\*\*（ps –aux）\*\*

13、结束后台进程的命令是\*\*（kill）\*\*

14、在 Linux 系统中，用来存放系统所需要的配置文件和子目录的目录是\*\*（/etc）\*\*

15 、Linux 使用支持 Windows 9.x/2000 长文件名的文件系统的类型是（vfat）

四、简答题  
1．（1）增加两个组账号 group1 、group2，并指定组账号 ID 分别为 10100 、10101  
**groupadd -g 10100 group1  
groupadd -g 10101 group2**

（2）增加二个用户账号 user1（UID 为 2045，并属于组 group1）、user2 （UID 为 2046，并属于组 group2） adduser -u 2045 -g group1 user1  
adduser -u 2046 -g group2 user2

2．（1）在用户 ray 个人目录下新建目录 **software， mkdir /home/ray/software**

（2）并搜索路径/etc 下所有以 h 开头的文件及目录，拷贝到 software 中 **cp /etc/h* /home/ray/software*\*

（3）请把目录 software 下所有内容建立压缩的 tar 包，并命名为 software.tar.gz  
tar -cvf software.tar.gz /home/ray/software

3．请按下列要求写出每一步骤的命令  
（1）新建普通用户 ray，并转为 ray 用户登录  
**useradd ray  
su ray**

（2）查看/etc/boot 路径下的所有内容  
**ls /etc/boot**

（3）查看文件/etc/hosts 的内容  
**ls /etc/hosts  
cat /etc/hosts**

4．（1）搜索 ray 个人目录下所有以 file 开头且属于 ray 用户的目录 **find /home/ray -user ray -name file**\*

（2）搜索 ray 个人目录下所有以file 开头且后跟一个字母的文件  
**find /home/ray -name file**\*

五．操作题  
1．Jack 一个人使用linux 系统，他既是系统管理员， 又是普通用户。为系统的稳定使用， 他需要使用管理 员账号为自己创建两个用户帐号 **tenny** 和**ten** ，**Jack** 平时使用这两个用户登陆使用系统， 为了这两个用户交 换和共享使用的方便，还需要达到如下要求：  
（1）在系统上建立一个目录―/myfile‖；  
**useradd tenny  
useradd ten  
mkdir /myfile**

（2）设置目录―/myfile‖的权限为：该目录里面的文件只能由 tenny 和 ten 两个用户读取、增加、删除、修 改和执行，其他用户不能对该目录进行任何访问操作。  
chmod -R 700 /myfile

1.Linux核心的许可证是什么？（ C ）  
A.NDA B.GDP **C.GPL** D.GNU

2.谁是Linux 的创始人（ D ）  
A.Turbolinux B. AT&T Bell Laboratry C. University of Helsinki **D. Linus Torvalds**

3.Linux 是操作系统意味着开放性源码 自 由 可 用 的 是 哪 个 选 项 ？ （ B ）  
A 封 闭 资 源 **B 开 放 资 源** C 用 户 注 册 D 开 放 性 二 进 制

4. 确 定 myfile 的 文 件 类 型 的 命 令 是 什 么 （ C ）  
   A. type myfile B. type -q myfile **C. file myfile** D. whatis myfile
5. 用 来 分 离 目 录 名 和 文 件 名 的 字 符 是 什 么 （ A ）  
   **A. slash (/)** B. period (.) C. dash (-) D. asterisk (\*)
6. 你 想 显 示 文 件 “longfile” 的 最 后 10 行 ， 下 面 那 个 命 令 是 正 确 的 （ A ）  
   **A. tail logfile** B. head － 10 longfile C. taid － d 10 longfile D. head longfile

7.假如你得到一个运行命令被拒绝的信息，你可以用哪个命令去修改它的权限使之可以正常运行（选择最 合 适 的 答 案 ） （B）  
a. path= **b. chmod** c. chgrp d. chown

8.拷贝 mydir\myfile 文件到 dir2目录下，但是系统提示这个文件已经存在，下面那个命令是正确的（选择最 合 适 的 答 案 ） （B）  
a 、 cp － w mydir\myfile dir2 **b 、 cp -i mydir\myfile dir2**  
c 、 cp mydir\myfile dir2 d 、 cp -v mydir\myfile dir2

9. 下 面 哪 个 命 令 允 许 对 文 件 重 命 名 （ 选 择 最 合 适 的 答 案 ）  
   a 、 rn b 、 rname c 、 replace  
   **d 、 mv**  
   答 案 d
10. 假 如 文 件 是 按 8 进 制 来 定 义 ， 下 面 哪 个 值 代 表 了 读 和 写 （ 选 择 最 合 适 的 答 案 ） a 、 2 **b 、 6** c 、 4 d 、 1  
    答 案 b

11.linux 临 时 目 录 一 般 存 在 下 面 哪 个 文 件 夹 中 （ 选 择 最 合 适 的 答 案 ）  
**a 、 /tmp** b 、 /proc c 、 /data d 、 /dev  
答 案 a

13. 下 面 哪 个 值 代 表 多 用 户 启 动 （ 选 择 最 合 适 的 答 案 ）  
    a 、 1 b 、 0 **c 、 3**  
    d 、 5  
    答 案 c
14. 下 面 哪 个 文 件 代 表 系 统 初 始 化 信 息 （ 选 择 最 合 适 的 答 案 ）  
    **a 、 /etc/inittab** b 、 /etc/init c 、 /etc/proc d 、 /etc/initproc  
    答 案 a
15. 哪 条 命 令 从 当 前 系 统 切 换 到 启 动 级 别 1 （ 选 择 最 合 适 的 答 案 ）  
    a 、 inittab 1 **b 、 init 1** c 、 level 1 d 、 rlevel1  
    答 案 b
16. 下 面 哪 个 选 项 能 取 消 shutdown 命 令 （ 选 择 最 合 适 的 答 案 ）  
    **a 、 shutdown －** c b 、 shutdown － x c 、 shutdown － u d 、 shutdown － n  
    答 案 a
17. 通 过 shell 执 行 一 个 命 令 ， 必 须 先 敲 入 一 个 \_\_\_\_\_ （ 选 择 最 合 适 的 答 案 ）  
    a. 参 数 **b. 命 令** c. 操 作 符 d. 终 端 ID 号  
    答 案 B
18. 哪 个 符 号 加 在 命 令 后 面 可 以 在 后 台 执 行 程 序 （ 选 择 最 合 适 的 答 案 ）  
    a. @ **b. &** c. # d. \*  
    答 案 B
19. 在 vi 编 辑 器 里 ， 哪 个 命 令 能 将 光 标 移 到 第 200 行 （ 选 择 最 合 适 的 答 案 ） a. 200g **b. :200**
20. c. g200
21. d. G200  
    答 案 b
22. 用 vi 打 开 一 个 文 件 ， 如 何 用 字 母 ‖new‖ 来 代 替 字 母 ‖old‖ （ 选 择 最 合 适 的 答 案 ）  
    a. :r/old/new b. 😒/old/new  
    **c. :1,$s/old/new/g**  
    d. 😒/old/new/g  
    答 案 c
23. 下 面 哪 个 配 置 文 件 用 来 定 义 syslog 的 后 台 进 程 （ 选 择 最 合 适 的 答 案 ） a 、 system.conf  
    **b 、 syslog.conf**

c 、 syslogd

d 、 slog.conf  
答 案 b

24. 下 面 哪 个 syslog.conf 代 表 httpd 进 程 （ 选 择 最 合 适 的 答 案 ）  
    a httpd b 、 proc c 、 smtp  
    **d 、 daemon**  
    答 案 d

23.你给公司的新同事添加一个用户，你起初指定他的帐号在30天后过期，现在想改变这个过期时间，用下 面 哪 个 命 令 （ 选 择 最 合 适 的 答 案 ）  
a 、 usermod － a b 、 usermod － d c 、 usermod － x

**d 、 usermod － e**  
答 案 d

24. 用 下 面 哪 个 命 令 可 以 不 用 退 出 vi 编 辑 器 来 切 换 文 件 （ 选 择 最 合 适 的 答 案 ）  
    **a. :e for edit command**  
    b. map command  
    c. export command  
    d. set command  
    答 案 a
25. 下 面 哪 个 选 项 用 来 添 加 用 户 定 义 用 户 登 录 的 shell （ 选 择 最 合 适 的 答 案 ）  
    **a 、 － s**  
    b 、 － u  
    c 、 － l  
    d 、 － sh  
    答 案 a
26. 如 果 你 想 给 变 量 “IQ” 定义为 4 ， 下 面 哪 些 时 正 确 的 （ 选 择 最 合 适 的 答 案 ）  
    a 、 IQ=4 b 、 set IQ=4  
    **c 、 set $IQ=4**  
    d 、 IQ set 4  
    答 案 c?
27. 在 系 统 重 建 的 时 候 ， 下 面 哪 个 参 数 能 用 来 对 mkfs 命 令 检 查 坏 块 （ 选 择 最 合 适 的 答 案 ）  
    a 、 － b b 、 － e  
    **c 、 － c**

d 、 － check  
答 案 c

28.哪 一 个 命令 能 用 来查 找在 文 件 TESTFILE 中只包含四个字符的行 ? （ 选 择最合 适 的 答 案 ）  
a.grep ‘???’ TESTFILE b.grep ‘…’ TESTFILE c.grep ‘^???$’ TESTFILE

**d.grep ‘^…$’ TESTFILE**  
答 案 d

29. 哪 一 个 命 令 能 用 来 删 除 当 前 目 录 及 其 子 目 录 下 名 为 ‗core’ 的 文 件 ? （ 选 择 最 合 适 的 答 案 ）  
    a.find . -name core -exec rm ;

**b.find . -name core -exec rm {} \ ;**

c.find . -name core -exec rm {} -; d.find . -name core -exec rm {} ;  
答 案 b

31.用 标 准 的输 出 重 定向 （ > ） 像 “> file01” 能 使 文 件 file01 的数 据 \_\_\_\_\_ （ 选 择 最合 适 的 答 案）  
a. 被 复 制 b. 被 移 动 c\*\*. 被 覆 盖\*\* d. 被 打 印  
答 案 c

33. 下 面 对 Linux 命 令 的 描 述 哪 个 是 正 确 的 （ 选 择 最 合 适 的 答 案 ）  
    a. 不 是 大 小 写 敏 感 的 b. 都 是 大 写 的  
    **c. 大 小 写 敏 感** d. 都 是 小 写  
    答 案 c
34. 在 vi 编 辑 器 里 ， 命 令 ‖dd‖ 用 来 删 除 当 前 ？ （ 选 择 最 合 适 的 答 案 ）  
    a. 字 b. 字 符 c. 变 量 **d. 行**  
    答 案 d

35.下列哪一个命令能被用来重定向管道的输出到标准输出和指定的文件中? （选择最合适的答案）  
a.cat  
b.less **c.tee**  
d.wee  
答 案 c

36.spool 文 件 系 统 放 到 什 么 位 置 （ 选 择 最 合 适 的 答 案 ）  
a 、 /proc b 、 /spool

**c 、 /var**

d 、 /lpd  
答 案 c

37. 下 面 哪 个 命 令 能 去 掉 主 引 导 信 息 里 的 内 容 （ 选 择 最 合 适 的 答 案 ）  
    **a 、 fdisk /mbr** b 、 format /mbr c 、 mbr/format d 、 mbr/replace  
    答 案 a
38. 下 面 哪 条 命 令 可 以 显 示 交 换 内 存 （ 选 择 最 合 适 的 答 案 ）  
    a 、 showmem b 、 freemem c 、 swap **d 、 free**  
    答 案 d
39. 下 面 哪 条 命 令 可 以 显 示 用 户 默 认 设 置 （ 选 择 最 合 适 的 答 案 ）  
    a 、 useradd － u b 、 show defaults c 、 show user defaults  
    **d 、 useradd -D**  
    答 案 d
40. 下 面 哪 段 定 义 了 添 加 一 个 tar 文件的信息（选择最合适的答案）  
    a 、 use the append command b 、 use the add command c 、 use the tar command with the -a switch  
    **d 、 use the tar command with the -r switch**  
    答 案 d
41. 在 vi 中 下 列 哪 些 命 令 不 能 用 来 在 光 标 前 插 入 文 本 ?( 选 择 所 有 正 确 的 )  
    **a. p [text] b. a [text]** c. i [text] **d. o [text]**  
    答 案 abd
42. 关 于 linux 下 列 说 明 哪 些 是 正 确 的 ? ( 选 择 所 有 正 确 的 )  
    **a. Linux 是 一 个 开 放 源 码 的 操 作 系 统 . b. Linux 是 一 个 类 UNIX 的 操 作 系 统 . c. Linux 是 一 个 多 用 户 的 操 作 系 统 . d. Linux 是一个 多任务 的 操 作 系 统 .**  
    答 案 abcd
43. 下 列 哪 些 叙 述 是 正 确 的 ? ( 选 择 所 有 正 确 的 )  
    **a. 在 DOS 下 可 以 用 命 令 rawrite 创建安装磁盘** . b. 在 DOS 下 可 以 用 命 令 dd 创建安装磁盘 .  
    **c. 通 常 可 以 从 可 引 导 的 CDROM 中安装 TurboLinux 系 统** . d. “rawrite” 可以在 linux 中运行 .  
    答 案 ac
44. 哪 些 命 令 组 合 起 来 能 统 计 多 少 用 户 登 录 系 统 （ 选 择 所 有 正 确 的 答 案 ）  
    a.who | wc -w  
    **b.who | wc -l c.who | wc -c  
    d.who | wc**  
    答 案 bd
45. 如果你对 文 件 和 目 录 的 权 限 不 确 定 , 则 不 能 用 \_\_\_\_\_\_\_ 命令来检测权限 .( 选 择 所 有 正 确 的 )  
    **a. ps**  
    b. ls -l  
    **c. ck  
    d. chown**  
    答 案 acd
46. 下面哪些 环境变量 是 在 Turbolinux shell 下被定义的？（选择所有合适的答案）  
    **a. PATH b. CD c. PS1**  
    d. TERM  
    答 案 abc

47 创 建 一 个 用 户 帐 号 需 要 在 /etc/passwd 中 定 义 哪 些 信 息 （ 选 择 所 有 合 适 的 答 案 ）  
**a 、 login name** b 、 password age  
**c 、 default group** **d 、 userid**  
答 案 ： a c d

48. 在本地的 文 件 系 统 中下列哪些 linux 路径结构是无效的 ?( 选 择 所 有 正 确 的 )  
    **a. //usr\zhang/memo b. \usr\zhang\memo**  
    c. /usr/zhang/memo  
    **d. \usr/zhang/memo**  
    答 案 a b d

49.Turbolinux 支 持 哪 些 编 程 语 言 （ 选 择 所 有 合 适 的 答 案 ）  
**a.Perl b.Python c.C++ d.Fortran**  
答 案 abcd

50.echo 命 令 可 以 用 来 显 示 ? （ 选 择 所 有 合 适 的 答 案 ） a. 参 数  
**b. 文 本 字 符** c. 过 滤 内 容  
**d. shell 变 量**  
答案 bd

一、单选

1. 一个硬盘最多能够被分成\_\_\_\_个主分区。 (D)  
   A. 1  
   B. 2  
   C. 3  
   **D. 4**
2. 一台 PC 上可以有两个 IDE 接口(将其称为第一 IDE、第二 IDE)，而且每个 IDE 接口上可以接两个 IDE 设备(将其称为主盘、从盘)。在 Linux 中，对第二 IDE 的主盘的命名名称为\_\_\_\_ 。©  
   A. /dev/hda  
   B. /dev/hdb  
   **C. /dev/hdc**  
   D. /dev/hdd
3. 在 UNIX/LINUX 系统中，将所有的设备都当做一个文件，放在\_\_\_\_ 目录下。 (B)  
   A. /bin  
   **B. /dev**  
   C. /etc  
   D. /usr
4. Linux 下的分区命名规则， 此处以第一个 IDE 的主盘为例。扩展分区中的逻辑分区是从\_\_\_\_开始编号的。  
   (D)  
   A. hda2  
   B. hda3  
   C. hda4  
   **D. hda5**
5. 关于 swap 分区，下面哪一条语句的叙述是正确的。 (D)  
   A. 用于存储备份数据的分区  
   B. 用于存储内存出错信息的分区  
   C. 在 Linux 引导时用于装载内核的分区  
   **D. 作为虚拟内存的一个分区**
6. 如果一台计算机有64MB 内存和100MB swap 空间，那么它的虚拟内存空间有多少呢？ (D)

A. 36MB  
B. 64MB  
C. 100MB  
**D. 164MB**

10. 按\_\_\_\_组合键可在应用程序窗口间实现切换。 ©  
    A. Shift+Tab  
    B. Ctrl+Alt+Tab  
    **C. Alt+Tab**  
    D. Ctrl+Tab
11. 对于 WINDOWS 操作系统，内存的多少对于系统的速度有很大的影响，于是增加内存就成为系统升级 的首选。为了保证你的计算机的内存达到够用好用的标准， 而且不产生不必要的浪费。用户通常可采用下 面哪一种工具来定量测量你的系统需要多少内存。 (D)  
    A. 系统策略编辑器  
    B. 系统配置实用程序 msconfig.exe  
    C. 系统诊断工具 Dr. Watson  
    **D. 系统监视器**
12. Linux 操作系统的创始人和主要设计者是： (D)  
    A. 蓝点 Linux  
    B. AT&T Bell 实验室  
    C. 赫尔辛基大学  
    **D. Linus Torvalds**
13. Linux 内核遵守的是下面哪一种许可条款。 ©  
    A. GDK  
    B. GDP  
    **C. GPL**  
    D. GNU
14. 目前市场上各种流行的 Linux 发行版本除少数外大多采用哪种格式的打包系统。 (A)  
    **A. RPM**  
    B. deb  
    C. zip  
    D. tar
15. 在 Linux 中，系统管理员(root)状态下的提示符是： (B)  
    A. $  
    **B. #**  
    C. %  
    D. >
16. Linux 带有一个名为 LILO(LInux LOad)的引导管理程序， LILO 的配置文件是： (D)  
    A. /usr/lilo.sys  
    B. /etc/lilo.sys  
    C. /usr/lilo.conf  
    **D. /etc/lilo.conf**
17. 在命令行中可以使用\_\_\_\_组合键来中止(kill)当前运行的程序。 (B)  
    A. Ctrl+d  
    **B. Ctrl+c**  
    C. Ctrl+u  
    D. Ctrl+q
18. 默认情况下， Linux 提供有六个虚拟控制台。当运行完 X Window 后， 应按什么键来切换到这六个虚拟 控制台。 (B)  
    A. Alt+Fn(n 为1-6之间的数字， 代表第几个虚拟控制台)  
    **B. Ctrl+Alt+Fn(n 为1-6之间的数字，代表第几个虚拟控制台)**  
    C. Ctrl+Shift+Fn(n 为1-6之间的数字，代表第几个虚拟控制台)  
    D. Shift+Fn(n 为1-6之间的数字，代表第几个虚拟控制台)
19. 在 Linux 中，完整路径中的目录间分隔符是： (A)  
    **A. /**  
    B.   
    C. |  
    D. -
20. 在 Linux 中，要求将文件 mm.txt 的所有使用者的文件执行权限删除。则下面所示命令中，哪一个是错 的。 (B)  
    A. chmod a-x mm.txt  
    **B. chmod o-x mm.txt**  
    C. chmod -x mm.txt  
    D. chmod ugo-x mm.txt
21. 下面哪一条命令可被用来关闭 Linux 系统。 (A)  
    **A. init 0**  
    B. init 1  
    C. init 5  
    D. init 6
22. 在 Linux 系统中，下面哪一条命令可被用来把大写字母转换成小写字母形式。 ©  
    A. upper  
    B. translate  
    **C. tr**  
    D. lower
23. 在 vi 全屏幕文本编辑器中，在指令模式下键入哪条命令将实现文件的不保存强制退出效果。 (B)  
    A. :q  
    **B. :q!**  
    C. :x  
    D. ZZ
24. 当使用 vi 编辑一个文件时，在指令模式下，下面哪条命令能复制当前行的内容到剪贴板中。 ©  
    A. cc  
    B. dd  
    **C. yy**  
    D. Ctrl+c
25. 在 Linux 中，如果当前目录是/home/sea/china，则下面哪一个目录是 china 目录的父目录。(A)  
    **A. /home/sea**  
    B. /home/  
    C. /  
    D. /sea
26. 当你登录 Linux 后，一个带有被称作\_\_\_\_ 的数字进程号的脚本被启动。 (A)  
    **A. PID**  
    B. UID  
    C. NID  
    D. CID
27. 在 Linux 中，下面哪一条命令可更改普通用户为超级用户。 (B)  
    A. super  
    **B. su**  
    C. tar  
    D. passwd
28. 关于 Linux 中的命令―shutdown -k‖ ，下面的哪一条叙述是正确的。 (A)  
    **A. 发送一条警示消息到所有用户**  
    B. 在重启动系统时跳过―fsck‖过程操作  
    C. 在关闭系统时跳过―init‖过程操作  
    D. 取消正在运行的关闭(shutdown)操作过程
29. Linux 允许一个文件名有256个字符，但为了保证兼容性和可移植性，建议你把文件名长度控制在\_\_\_\_ 个字符以内。 ©  
    A. 8  
    B. 12  
    **C. 14**  
    D. 16
30. 在 Linux 系统中，通过使用文件链接命令(ln)功能，可实现一个文件被下述哪种形式来处理。 (D)  
    A. 仅一个文件名称  
    B. 不超过两个文件名称  
    C. 每个目录可有一个文件名称  
    **D. 两个或更多个文件名称**
31. 大部分主要的 Linux 系统文件是存放在下面的哪个目录之中的。 (A)  
    **A. /bin**  
    B. /tmp  
    C. /lib  
    D. /root
32. Linux 标准 c 和 c++编译器是\_\_\_\_ 。©  
    A. tc  
    B. cc  
    **C. gcc**  
    D. gdb
33. 下面哪条命令可以使 shell 变量变为一个全局变量。 (D)  
    A. alias  
    B. exports  
    C. exportfs  
    **D. export**
34. 在一个 bash shell 脚本的第一行上应加入下面所示中的哪一条语句。 (D)  
    A. #/bin/csh  
    B. #/bin/bash  
    C. /bin/bash  
    **D. #!/bin/bash**
35. Linux 命令行是由\_\_\_\_提供的。 (D)  
    A. 管道  
    B. 分层结构文件系统  
    C. 文本处理器  
    **D. shell**
36. 你可编制一个由一系列命令组成的程序，该程序可由 shell 执行。这种类型的程序被称作―\_\_\_\_‖ 。(B)  
    A. shell 变量  
    **B. shell 脚本**  
    C. 管道  
    D. shell 语法
37. 要从 shell 命令行中执行一条命令，你必须首先键入\_\_\_\_ 。(B)  
    A. 参数变量  
    **B. 命令名**  
    C. 选项  
    D. 终端号
38. 用户要想在后台执行程序，则你需在命令行的末端放置哪个字符。 (B)  
    A. @  
    **B. &**  
    C. #  
    D. %
39. 下面哪条命令可把./dir1目录(包括它的所有子目录)内容复制到./dir2中？ (D)  
    A. cp -i ./dir1/\* ./dir2  
    B. cp -P ./dir1/\* ./dir2  
    C. cp -d ./dir1/\* ./dir2  
    **D. cp -r ./dir1/* ./dir2*\*
40. 哪条命令用来显示文件和目录占用的磁盘空间？(B)  
    A. df  
    **B. du**  
    C. ls  
    D. printenv
41. 下面哪条命令可被用来显示已安装文件系统占用的磁盘空间？ (A)  
    **A. df**  
    B. du  
    C. ls  
    D. mount
42. 安装 CD-ROM 时，默认选择哪种类型的文件系统？ (D)  
    A. vfat  
    B. ufs  
    C. ext2  
    **D. iso9660**
43. swap 文件与 swap 分区相比，它具有如下所叙述的哪条优点？ (B)  
    A. 更好的性能  
    **B. 可以更有效率地应用磁盘空间**  
    C. 更容易操作  
    D. 没有突出的优点
44. 如果在/etc/group 文件中有一行内容是―students::600:z3,l4,w5‖，那么在―students‖组中有多少个用户？ (D)  
    A. 3  
    B. 4  
    C. 5  
    **D. 不清楚**
45. /etc 文件系统的标准应用是用于\_\_\_\_ ？(D)  
    A. 安装附加的应用程序  
    B. 存放可执行程序、系统管理工具和库  
    C. 设置用户的主目录  
    **D.用于存放系统管理的配置文件**
46. 在安装 Linux 操作系统过程中你可以选择下面哪种形式来登录？ (D)  
    A. 选择―图形登录‖在级别4层次设置系统起始模式  
    B. 选择―文本登录‖在级别5层次设置系统起始模式  
    C. 选择―图形登录‖在级别3层次设置系统起始模式  
    **D. 选择―文本登录‖在级别3层次设置系统起始模式**
47. 在 ext2文件系统中，一个目录数据块中的指针指向的是\_\_\_\_ 。©  
    A. 目录中的子目录和文件  
    B. 目录的其它数据块  
    **C. 目录的 i 节点**  
    D. 该目录的父目录
48. 在 Linux shell 中，下面哪个变量代表的是 shell 程序命令的程序文件名。 ©  
    A. $#  
    B. $\*  
    **C. $0**  
    D. $$
49. 键入下面所述的哪个组合键，可以退出 X Window 。(D)  
    A. Alt+F4  
    B. Ctrl+Backspace  
    C. Ctrl+Alt+F4  
    **D. Ctrl+Alt+Backspace**

二、多项选择  
50. 硬盘分区是针对一个硬盘进行操作的，它可以分为： ****、**** 、\_\_\_\_ 。(D,A,C)  
**A. 扩展分区**  
B. 物理分区  
**C. 逻辑分区**  
**D. 主分区**  
51. 目前, 在 PC 机上使用的电源管理模式主要有： (A,C)  
**A. APM 管理模式**  
B. PM 管理模式  
**C. ACPI 管理模式**  
D. DPMS 管理模式

52. Linux 系统必须至少要创建哪些分区： (A,B)  
    **A. 根分区(/)  
    B. 交换(swap)分区**  
    C. 扩展分区  
    D. 逻辑分区

    7. 假设用户当前目录是： /home/xu ，现需要返回到用户主目录，则下面哪几种命令可实现这一目的。 (A，C,D)

**A. cd $HOME  
C. cd  
D. cd ~**  
53. 系统用户帐户信息被贮藏在下面哪些文件中。(B，C)

54. 要成功登录 Linux 系统，至少需要哪些必备条件。 (A,B)  
    A. 登录 ID 号  
    B. 默认登录 shell  
    C. 登录(用户)主目录  
    D. 一个独一无二的网络识别号
55. 关于―umount‖命令操作的描述，下面哪些描述是错误的。 (A,B,C,D)  
    A. 你可以在卸载之前把软盘取出  
    B. 你应该在卸载之前把 CD 盘取出  
    C. 默认情况下，普通用户可以使用该命令  
    D. 默认情况下， root 用户可以使用该命令卸载任何路径中的任何文件系统。
56. 关于―符号链接‖的叙述，下面哪些叙述是正确的？ (A,B,C,D)  
    **A. 它可以链接到一个目录  
    B. 它可以链接到一个设备文件  
    C. 它可以链接到一个不存在的文件  
    D. 它可以链接到另一个文件系统的一个文件**
57. 下面关于文件/etc/group 的功能的描述，哪些是正确的？ (A,B)  
    **A. 把用户分配到各个组**  
    **B. 为每个组号设置一个组名**  
    C. 存放用户口令  
    D. 规定哪个用户可以处理诸如打印机之类的网络资源

一、选择题  
1.在创建Linux分区时，一定要创建（ D ）两个分区  
A. FAT/NTFS  B. FAT/SWAP  C. NTFS/SWAP  D.SWAP/根分区

2.在Red Hat Linux 9 中，系统默认的（A）用户对整个系统拥有完全的控制权。  
A. root  B. guest  C. administrator  D.supervistor.

3.当登录Linux时，一个具有唯一进程ID号的shell将被调用，这个ID是什么( B )  
A. NID B. PID C. UID D. CID

4.下面哪个命令是用来定义shell的全局变量( D )  
A. exportfs B. alias C. exports D. export

5.哪个目录存放用户密码信息( B )  
A. /boot B. /etc C. /var D. /dev

6.默认情况下管理员创建了一个用户，就会在( B )目录下创建一个用户主目录。  
A. /usr B. /home C. /root D. /etc

7.当使用mount进行设备或者文件系统挂载的时候，需要用到的设备名称位于( D )目录。  
A. /home B. /bin C. /etc D. /dev

8.如果要列出一个目录下的所有文件需要使用命令行( C )。  
A. ls–l B. ls C. ls–a D. ls–d

9.哪个命令可以将普通用户转换成超级用户( D )  
A. Super B. passwd C. tar D. su

10.除非特别指定，cp假定要拷贝的文件在下面哪个目录下( D )  
A.用户目录 B. home目录 C. root目录 D.当前目录

11.在vi编辑器里，命令"dd"用来删除当前的( A )  
A.行 B.变量 C.字 D.字符

12.当运行在多用户模式下时，用Ctrl+ALT+F\*可以切换多少虚拟用户终端( B )

A. 3 B. 6 C. 1 D. 12

13.Linux启动的第一个进程init启动的第一个脚本程序是( B )。  
A./etc/rc.d/init.d B./etc/rc.d/rc.sysinit  
C./etc/rc.d/rc5.d D./etc/rc.d/rc3.d

14.按下( A ) 键能终止当前运行的命令  
A. Ctrl-C B. Ctrl-F C. Ctrl-B D. Ctrl-D

15.下面哪个命令用来启动X Window ( C )  
A. Runx B. Startx C. startX D. xwin

16.用来分离目录名和文件名的字符是( B )  
A. dash (-) B. slash (/) C. period (.) D. asterisk（\*）

17.用 “rm -i”,系统会提示什么来让你确认( B )  
A.命令行的每个选项 B.是否真的删除 C.是否有写的权限 D.文件的位置

18.以下哪个命令可以终止一个用户的所有进程( D )  
A. skillall B. skill C. kill D. killall

19.在Red Hat Linux 9中，一般用（ D ）命令来查看网络接口的状态  
A. ping B. ipconfig C. winipcfg D ifconfig

20.vi中哪条命令是不保存强制退出( C )  
A. :wq B. :wq! C. :q! D. :quit

21.在下列分区中，Linux默认的分区是（ B）  
A. FAT32 B. EXT3 C. FAT D. NTFS

22.若要将鼠标从VM中释放出来，可按 （ A）键来实现  
A. Ctrl + Alt B. Ctrl +Alt +Del C. Ctrl +Alt +Enter D Ctrl +Enter

23.如果用户想对某一命令详细的了解，可用（ C ）。  
A. ls B. help C. man D dir

24.Samba服务器的配置文件是 ( D )。  
A httpd.conf B inetd.conf C rc.samba D smb.conf

25.用户编写了一个文本文件a.txt，想将该文件名称改为txt.a，下列命令（ D ）可以实现。  
A.cd a.txt xt.a B. echo a.txt > txt.a  
B.rm a.txt txt.a D. cat a.txt > txt.a

26.Linux文件权限一共 10 位长度，分成四段，第三段表示的内容是（ C ）。  
A. 文件类型      B. 文件所有者的权限     
C. 文件所有者所在组的权限  D. 其他用户的权限

27.在使用mkdir命令创建新的目录时，在其父目录不存在时先创建父目录的选项是( D )。  
A. -m B. -d C. -f D. -p

28.下面关于节点描述错误的是 （ A ）。  
A．节点和文件是一一对应的 B．节点能描述文件占用的块数  
C．节点描述了文件大小和指向数据块的指针 D．通过节点实现文件的逻辑结构和物理结构的转换

29.在 vi 编辑器中的命令模式下，重复上一次对编辑的文本进行的操作，可使用 （ C ）命令。  
A. 上箭头 B. 下箭头 C. “.” D. “\*”

30.某文件的组外成员的权限为只读；所有者有全部权限；组内的权限为读与写，则该文件的权限为( D )。  
A. 467 B. 674 C. 476 D. 764

31.在Redhat公司发布的Linux版本中，若要使得用户登录验证，需要修改以下 （ C ）脚本。  
A. /etc/inittab B. /etc/passwd C. /etc/shadow D. /etc/group

32.下列不是 Linux 系统进程类型的是( D )。  
A.交互进程 B.批处理进程 C.守护进程 D.就绪进程

33.下列关于 /etc/fstab 文件描述，正确的是( D )。  
A.fstab文件只能描述属于linux的文件系统  
B. CD\_ROM和软盘必须是自动加载的  
B.fstab文件中描述的文件系统不能被卸载  
D.启动时按fstab文件描述内容加载文件系统

34.在 Shell 脚本中，用来读取文件内各个域的内容并将其赋值给 Shell 变量的命令是( D )。  
A. fold B. join C. tr D. read

35.Linux系统的开发模型是（  B  ）。  
A.教堂模型 B.集市模型 C.层次模型 D.网状模型

36.在 Linux 中，进程优先级的相关参数有多个，与实时进程优先级相关的参数是( D )。  
A.policy B.counter C.priority D.rt\_priority

37.在Linux系统中，每个进程都有4GB的虚拟地址空间，其中内核空间占用 （ C ）。  
A．0~2GB-1 B．0~3GB-1 C．3GB~4GB-1 D．2GB~4GB-1

38.Linux文件系统中，文件在外存的物理地址放在（  A  ）中。  
A.节点 B.用户打开文件表 C.系统打开文件表 D.进程控制块

39.以长格式列目录时，若文件test的权限描述为：drwxrw-r–，则文件test的类型及文件主的权限是（  A  ）。  
A.目录文件、读写执行 B.目录文件、读写  
C.普通文件、读写 D.普通文件、读

40.当字符串用单引号（’’）括起来时，SHELL将（ C ）。  
A.解释引号内的特殊字符 B.执行引号中的命令  
C.不解释引号内的特殊字符 D.结束进程

41./etc/shadow文件中存放（  B  ）。  
A.用户账号基本信息 B.用户口令的加密信息  
C.用户组信息 D.文件系统信息

42.Linux系统中，用户文件描述符 0 表示（  A  ）。  
A.标准输入设备文件描述符 B.标准输出设备文件描述符  
C.管道文件描述符 D.标准错误输出设备文件描述符

43.为卸载一个软件包，应使用（  B  ）。  
A.rpm -i B.rpm -e C.rpm -q D.rpm -V

44.若当前目录为 /home,命令 ls–l 将显示 home 目录下的（ D ）。  
A.所有文件 B.所有隐含文件 C.所有非隐含文件 D.文件的具体信息

45.下面关于文件 “/etc/sysconfig/network-scripts/ifcfg-eth0” 的描述哪个是正确的?( D )。  
A.它是一个系统脚本文件 B.它是可执行文件  
C.它存放本机的名字 D.它指定本机eth0的IP地址

46.如何快速切换到用户John的主目录下？( D )  
A.cd @John B.cd #John C.cd &John D.cd ~John

47.启动DNS服务的守护进程（ C ）  
A. httpd start B.httpd stop C. named start D. named stop

48.若URL地址为http://www.nankai.edu/index.html，请问哪个代表主机名( D )  
A.nankai.edu.cn B.index.html  
C.www.nankai.edu/index.html D.www.nankai.edu

49.在LINUX中，要查看文件内容，可使用（  A  ）命令。  
A.more        B.cd        C.login        D.logout

50.光盘所使用的文件系统类型为（  D  ）。  
A.ext2      B.ext3       C.swap        D.ISO 9660

51.LINUX 所有服务的启动脚本都存放在（  A  ）目录中。  
A./etc/rc.d/init.d    B./etc/init.d    C./etc/rc.d/rc    D./etc/rc.d

52.RED HAT LINUX 所提供的安装软件包，默认的打包格式为（  C  ）。  
A…tar        B…tar.gz        C…rpm         D…zip

53.以下文件中，只有 root 用户才有权存取的是（  B  ）  
A.passwd      B.shadow        C.group        D.password

54.usermod 命令无法实现的操作是（  B  ）  
A.账户重命名    B.删除指定的账户和对应的主目录   
C.加锁与解锁用户账户     D.对用户密码进行加锁或解锁

55.LINUX用于启动系统所需加载的内核程序位于（  C  ）  
A./   B./lib/modules/2.4.20\_8/kernel       C./boot       D./proc

56.init进程对应的配置文件名为（ D ），该进程是LINUX系统的第一个进程，其进程号PID始终为1。   
A./etc/fstab  B./etc/init.conf   
C./etc/inittab.conf     D./etc/inittab

57.在LINUX运行的7个级别中，X—WINDOWS图形系统的运行级别为（  C  ）。  
A.2          B.3           C.5           D.6

58.若在文字界面下，需要键入何种指令才能进入图形界面（Xwindow）。（  B ）  
A. reboot        B.startx  C.startwindow        D.getinto

59.当安装linux操作系统时将选择下列那一个操作? ( B )  
A. 选择 “图形登录方式” 设定系统开始运行级为4  
B. 选择 “文本登录方式” 设定系统开始运行级为3  
C. 选择 “文本登录方式” 设定系统开始运行级为5  
D. 选择 “图形登录方式” 设定系统开始运行级为3

60.Linux 通过 VFS 支持多种不同的文件系统。Linux缺省的文件系统是（ C ）  
A.VFAT       B.ISO9660         C.Ext系列          D.NTFS

61.关闭linux系统（不重新启动）可使用（  B ）命令。  
A.ctrl+alt+del        B.halt      C.shutdown  -r        D.reboot

62.修改以太网mac地址的命令为（ B ）。  
A.ping          B.ifconfig            C.arp           D.traceroute

63.在 vi 编辑器中的命令模式下，键入（ B ）可在光标当前所在行下添加一新行。  
A. “a”    B.“o”    C.“i”      D.“A”

64.以下选项中，哪个命令可以关机? ( A )  
A. init 0          B. init 1         C. init 5         D. init 6

65.请选择关于 /etc/fstab 的正确描述(  B  )。  
A. 系统启动后，由系统自动产生   
B. 用于管理文件系统信息  
C. 用于设置命名规则，是否使用可以用 TAB 来命名一个文件   
D. 保存硬件信息

66.你使用命令“vi /etc/inittab”查看该文件的内容，你不小心改动了一些内容，为了防止系统出问题，你不想保存所修改内容，你应该如何操作(   B  )  
A.在末行模式下，键入:wq       B.在末行模式下，键入:q!  
C.在末行模式下，键入:x!       D.在编辑模式下，键入“ESC”键直接退出vi

67.显示已经挂装的文件系统磁盘inode使用状况的命令是(  A  ) ?  
A.df –i             B.su –I           C.du –I        D.free –i

68.删除文件命令为(   D  )  
A.mkdir               B.move              C.mv                D.rm

69.网络管理员对www服务器可进行访问、控制存取和运行等控制，这些控制可在（  A  ）文件中体现。  
A.httpd.conf       B.lilo.conf     C.inetd.conf      D.resolv.conf

70.如果想在Linux下实现热启，应当修改/etc/inittab下的哪一行（ B ）。  
A.#Trap CTRL-ALT-DELETE   
B.#ca::ctrlaltdel :/sbin/shutdown -t3 -r now  
B.#id:3:initdefault:   
D.#10:3:wait:/etc/rc.d/rc 3

71.下列哪个命令在建立一个 tar归档文件的时候列出详细列表（ A ）。  
A.tar -t        B.tar -cv       C.tar -cvf       D.tar –r

72.假设文件fileA的符号链接为fileB，那么删除fileA后，下面的描述正确的是（ B ） 。  
A.fileB也随之被删除   
B.fileB仍存在，但是属于无效文件  
C.因为fileB未被删除，所以fileA会被系统自动重新建立   
D.fileB会随fileA的删除而被系统自动删除

73.一个bash shell脚本的第一行是（ D ）？  
A.#/bin/csh       B.#/bin/bash  C./bin/bash      D.#!/bin/bash

74.改变文件所有者的命令为（ C ）？  
A.chmod              B.touch              C.chown             D.cat

75.用于文件系统直接修改文件权限管理命令为：（  C  ）  
A. chown       B. chgrp  C. chmod       D. umask

76.在给定文件中查找与设定条件相符字符串的命令为（ A  ）。  
A.grep            B.gzip           C.find            D.sort

77.建立一个新文件可以使用的命令为（  D ）。  
A.chmod              B.more               C.cp            D.touch

78.存放Linux基本命令的目录是什么（ A  ）?  
A. /bin              B. /tmp          C. /lib           D. /root

79.自由软件的含义是（ B ）。  
A．用户不需要付费      B．软件可以自由修改和发布   
C．只有软件作者才能向用户收费   D．软件发行商不能向用户收费

80.系统引导的过程一般包括如下几步：a．MBR中的引导装载程序启动；b．用户登录；c．Linux内核运行；d．BIOS自检。正确的顺序是（ B ）。  
A．d,b,c,a     B．d,a,c,b      C．b,d,c,a   D．a,d,c,b

81.字符界面下使用shutdown命令重启计算机时所用的参数是（ D ）。  
A．-h   B．-t      C．-k     D．-r

82.下列设备属于块设备的是（ D ）。  
A．键盘       B．终端  C．游戏杆      D．硬盘

83.cd 命令可以改变用户的当前目录，当用户键入命令 “cd” 并按Enter键后，（ C ）。  
A．当前目录改为根目录     B．当前目录不变，屏幕显示当前目录  
C．当前目录改为用户主目录   D．当前目录改为上一级目录

84.在UNIX/Linux系统添加新用户的命令是（  D  ）  
A. groupadd      B. usermod  C. userdel       D. useradd

85.添加用户时使用参数（ A ）可以指定用户目录。  
A. -d        B. -p  C. -u        D. -c

86.修改用户自身的密码可使用（ A ）  
A. passwd        B. passwd -d mytest   
C. passwd  mytest      D. passwd -l

87.统计磁盘空间或文件系统使用情况的命令是：(  A  )  
A. df        B. dd  C. du        D. fdisk

88.若使pid进程无条件终止使用的命令是（ A  ）。  
A. kill -9       B. kill -15  C. killall -1       D. kill -3

89.显示系统主机名的命令是（  C  ）  
A. uname -r      B. who am i  C. uname -n      D. whoami

90.Linux系统中用于打印队列查询的命令是（  D ）。  
A. lp        B. lprm  C. lpr      D. lpstat

91.202.196.100.1 是何类地址（  C ）  
A、A类       B、B类  C、C类       D、D类

92.当 IP 地址的主机地址全为 1 时表示：（  B  ）  
A、专用IP地址      B、对于该网络的广播地址   
C、本网络地址       D、回送地址

93.FTP传输中使用哪两个端口（  C  ）。  
A、23和24      B、21和22  C、20和21      D、22和23

94.欲把当前目录下的 file1.txt 复制为 file2.txt，正确的命令是（  D  ）。  
A. copy file1.txt file2.txt        B. cp file1.txt | file2.txt  
C. cat file2.txt file1.txt         D. cat file1.txt > file2.txt

95.如果您想列出当前目录以及子目录下所有扩展名为“.txt”的文件，那么您可以使用的命令是（  B  ）。  
A. ls \*.txt    B. find . –name “.txt”    
C. ls –d .txt        D. find . “.txt”

96.如何删除一个非空子目录 /tmp（  B  ）。  
A. del /tmp/\*    B. rm -rf /tmp      
C. rm -Ra /tmp/\*    D. rm –rf /tmp/\*

97.存放用户帐号的文件是（  C  ）。  
A. shadow     B. group         C. passwd         D. Gshadow

98.一个文件名字为rr.Z，可以用来解压缩的命令是（  D  ）  
A．tar         B. gzip          C. compress          D. uncompress

99.如果执行命令 #chmod 746 file.txt，那么该文件的权限是（  A    ）。  
A. rwxr–rw-    B. rw-r–r--    C. --xr—rwx       D. rwxr–r—

100.Linux有三个查看文件的命令，若希望在查看文件内容过程中可以用光标上下移动来查看文件内容，应使用命令（  C  ）  
A．cat           B. more          C. less           D. menu

101.若一台计算机的内存为128MB，则交换分区的大小通常是（  C  ）  
A．64MB           B. 128MB          C. 256MB           D. 512MB

102.用ls –al 命令列出下面的文件列表，是符号连接文件的是（  D  ）  
A．-rw-rw-rw- 2 hel-s users 56 Sep 09 11:05 hello

B．-rwxrwxrwx 2 hel-s users 56 Sep 09 11:05 goodbey

C．drwxr–r-- 1 hel users 1024 Sep 10 08:10 zhang

D．lrwxr–r-- 1 hel users   7 Sep 12 08:12 cheng

103.文件 exer1 的访问权限为rw-r–r–，现要增加所有用户的执行权限和同组用户的写权限，下列命令正确的是（ A ）  
A．chmod a+x, g+w exer1     B．chmod 765 exer1   
C．chmod o+x exer1          D．chmod g+w exer1

104.关闭linux系统（不重新启动）可使用-命令（ C ）  
A．ctrl+alt+del    B．shutdown  -r     C．halt    D．reboot

105.对文件进行归档的命令为（ B   ）  
A．gzip          B．tar        C．dump          D．dd

106.NFS是（  C  ）系统  
A．文件         B 磁盘        C．网络文件      D．操作

107.下列那一个指令可以显示目录的大小（  C  ）  
A．dd           B．df          C．du            D．dw

108.下列那一个不是压缩指令（  D  ）  
A．compress   B．gzip        C．bzip2         D．tar

109.下列那一个指令可以用来切换至不同的 runlevels（  B  ）  
A．tel        B telinit      C．goto          D．reboot

110.下列那一个指令可以用来查看系统负载情形（  A   ）  
A．w          B．who      C．load           D．ps

111.档案权限 755 , 对档案拥有者而言, 何义（  A  ）  
A．可读,可执行, 可写入     B 可读       C．可读,可执行      D．可写入

112.下面哪个系统目录中存放了系统引导、启动时使用的一些文件和目录 （ D ）。  
A./root        B. /bin          C. /dev           D. /boot

113.如何删除目录 /tmp下的所有文件及子目录（  D  ）。  
A. del /tmp/\*    B. rm -rf /tmp       
C. rm -Ra /tmp/\*    D. rm –rf /tmp/\*

114.可以用来对文件xxx.gz解压缩的命令是（ C ）  
A．compress    B. uncompress    C. gunzip            D. tar

115.对文件重命名的命令为（ C ）  
A．rm           B. move        C. mv               D. mkdir

二、填空题  
1.将前一个命令的标准输出作为后一个命令的标准输入，称之为管道。  
2.在 shell编程时，使用方括号表示测试条件的规则是:方括号两边必有空格。  
3.在Linux系统下，第二个IDE通道的硬盘（从盘）被标识为 hdb 。  
4.当系统管理员需升级内核版本和改变系统硬件配置时，应重新编译内核。  
5.在 Linux系统中，测试DNS 服务器是否能够正确解析域名的的客户端命令，使用命令nslookup 。  
6.启动进程有手动启动和调度启动两种方法，其中调度启动常用的命令为at .batch和\*\* crontab\*\* 。  
7.在 Linux 操作系统中，设备都是通过特殊的文件来访问。  
8.shell 不仅是用户命令的解释器，它同时也是一种功能强大的编程语言。  
9.在Windows9.x环境下共享Unix/Linux 中的用户目录的一个工具是samba服务器。  
10. 结束后台进程的命令是kill。  
11. 在Linux的两种链接文件中，只能实现对文件链接的一种方式是:软链接(符号链接)。  
12. Linux 主要采用了请求调页和写时复制两种动态内存管理技术实现了物理内存以on demand方式动态分配。  
13. 对于System V类型的共享内存页面，Linux基于Clock算法决定哪些页面应当被换出物理内存。  
14. 在 Linux与中断相关的三个核心数据结构中，用做抽象的中断控制器的数据结构是hw interrupt type，它包含一系列处理中断控制器特有的操作。  
15. 通过将request动态链入块设备控制结构blk dev struct，Linux设备管理器有效的实现了物理设备和缓冲区之间的异步读写通讯。  
16. 将/home/stud1/wang目录做归档压缩，压缩后生成wang.tar.gz文件，并将此文件保存到/home目录下，实现此任务的tar 命令格式tar -czvf wang.tar.gz /home  
/stud1/wang。  
17. 对于给定的文件file,统计其中所有包含字符串”WHU"的行数的一条命令是grep WHU file wc -l。  
18. 对于Shell脚本程序，若输入参数数量多于9 个，则程序遍历每个参数可通过使用shift命令实现。  
19. 在SystemV进程通讯方式中，ipc\_perm结构描述对一个系统IPC对象的存取权限，而用于定位.IPC对象的引用标志符key可以依据键值分成公有和私有两种类型。  
20. 默认情况下，超级用户和普通用户的登录提示符分别是: “#”和”$”。  
21. Linux内核引导时，从文件\*\*/etc/fstab中读取要加载的文件系统。  
22. Linux系统下经常使用的两种桌面环境是: GNOME和KDE\*\*。  
23. 链接分为:硬链接和符号链接。  
24. Linux系统中有三种基本的文件类型:普通文件、目录文件和设备文件。  
25. 某文件的权限为: drw-r–r–，用数值形式表示该权限，则该八进制数为:644 ,  
该文件属性是目录。  
26. 在超级用户下显示Linux系统中正在运行的全部进程，应使用的命令及参数是ps -aux。  
27. /sbin目录用来存放系统管理员使用的管理程序。  
28. 观察当前系统的运行级别可用命令: who -r实现。  
29. grep -E’[Hh]enr(y|ietta)’ file的功能是:在文件File中查找Henry、henry、Henrietta或henrietta。  
30. vi编辑器具有三种工作模式，即:命令模式、文本编辑模式和行编辑模式。  
31. linux文件系统中每个文件用 i节点 来标识。  
32. 前台启动的进程使用复合键CTRL+C 终止。  
33. 增加一个用户的命令是useradd。  
34. 成批添加用户的命令是newuser。  
35. 在Linux2.4.0版本中，进程有6种状态，进程使用exit系统调用后进入僵死状态。  
36. 在Linux 中，管道分为2种类型，若创建或打开管道时获得的描述符存放在fd中，则fd[1]是管道写描述符。  
37. Linux为用户提供的接口有shell、XWINDOW、系统调用。  
38. Linux在I386体系结构中支持两级分页机构。  
39. 每个设备文件名由主设备号和从设备号描述。第二块IDE硬盘的设备名为hdb，它上面的第三个主分区对应的文件名是 hdb3 。  
40. 超级块是描述文件系统属性信息的数据结构,索引节点是描述文件属性信息的数据结构。  
41. df 命令完成显示文件系统空间使用情况功能，du命令完成显示目录或文件占用磁盘空间容量功能。  
42. 命令组合（命令表）将建立新的子进程来执行命令。  
43. 磁盘限额管理可以使用quota软件工具,其中硬限额的容量应该大于软限额。  
44. 交换线程通过三种途径来缩减已使用的内存页面:减少 buffer cache和 page cache的大小、换出系统V类型的内存页面、换出或丢弃进程的页面。  
45. 在Linux系统中，压缩文件后生成后缀为.gz文件的命令是gzip。  
46. RPM有5种基本操作模式，即:安装、查询、校验、升级、删除。  
47. 将当前目录下的文件 man.config压缩为man.config.bz2的命令是 bzip2 -z man.config。  
48. 将/home/stu目录下所有的.gz压缩文件解压缩，包括子目录,命令是gunzip -r /home/stu。  
49. 将当前目录下的 bin目录和 hello 、 hello.c文件备份并压缩为binzxj.tar.gz文件的命令是tar -czvf binzxj.tar. gz bin hello hello.c。  
50. 将/home/ixdba目录做归档压缩，压缩后生成ixdba.tar.bz2文件，并将此文件保存到/home目录下，实现此任务的 tar命令格式tar -cjvf /home/ixdba.tar.bz2 /home/ixdba。  
51. 设定限制用户使用磁盘空间的命令是quota 。  
52. 在Linux系统中,用来存放系统所需要的配置文件和子目录的目录是\*\*/etc\*\*。  
53. 为脚本程序指定执行权的命令及参数是 chmod a+x filename。  
54. 进行字符串查找，使用grep 命令。  
55. 在 Linux系统中，以文件的方式访问设备。  
56. 静态路由设定后，若网络拓扑结构发生变化，需由系统管理员修改路由的设置。  
57. 网络管理的重要任务是:控制和监控。  
58. 安装Linux系统对硬盘分区时，必须有两种分区类型:文件系统分区和交换分区。  
59. 编写的Shell程序运行前必须赋予该脚本文件执行权限。

三、简答题  
1.请简述Linux操作系统有什么优点？  
答：Linux的主要优点包括：  
·提供了先进的网络支持：内置TCP/IP协议；  
·真正意义上的多任务、多用户作系统；  
·与UNIX系统在源代码级兼容，符合IEEE POSIX标准；  
·支持数十种文件系统格式；  
·开放源代码，用户可以自己对系统进行改进；  
·采用先进的内存管理机制，更加有效地利用物理内存。

2.简述Linux文件系统通过i节点把文件的逻辑结构和物理结构转换的工作过程。  
答：Linux通过i节点表将文件的逻辑结构和物理结构进行转换  
i节点是一个64字节长的表，表中包含了文件的相关信息，其中有文件的大小、文件所有者、文件的存取许可方式以及文件的类型等重要信息。  
在i节点表中最重要的内容是磁盘地址表。在磁盘地址表中有13个块号，文件将以块号在磁盘地址表中出现的顺序依次读取相应的块。若文件空间大于13块，则分别用1次、2次、3次间接块实现对数据块的定位。  
此后，Linux文件系统通过把i节点和文件名进行连接，当需要读取该文件时，文件系统在当前目录表中查找该文件名对应的项，由此得到该文件相对应的i节点号，通过该i节点的磁盘地址表把分散存放的文件物理块连接成文件的逻辑结构。

3.vi 编辑器有哪几种工作模式？如何在这几种工作模式之间转换？  
答：Vi的工作模式有三种：命令模式、输入模式、末行模式。  
在命令模式下输入a、A、i、I、o、O等命令之一可以进入输入模式，  
在输入模式下按Esc键回到命令模式；  
在命令模式下输入：进入末行模式，  
末行命令执行完后回到命令模式。

4.什么是位置变量？shell的变量类型有哪些种？  
答：位置变量是指命令行上传递给程序的参数。  
Shell变量可以分为：用户自定义变量、环境变量、位置变量、特殊变量

5.从内核实现的角度说明 Linux 进程共享文件的方式有哪几种？举例说明什么情况下会产生对应的共享情况？  
答：进程通过多个 file 结构共享一个 inode，进程共享一个 file 结构。

6.试述如何创建一个用户。  
答：可使用命令useradd创建新用户，但不能在系统中随便创建用户，需经相关部分批准后方能创建。对于长期或暂时不使用的用户，应将其从系统中删除或锁定起来，以防非法使用。创建新用户时可以使用命令useradd -d home newuser指定用户家目录，若不指定则使用默认的家目录/home/newuser。一般情况下，当一个用户被创建之后，只有超级用户为它设置密码后才能被启用或登录使用。

7.Linux系统有几种类型文件？它们分别是什么？有哪些相同点和不同点？  
答：3类。分别是普通文件，目录文件和设备文件。  
相同是它们都是文件，都有一个文件名和i节点号。  
不同点是，普通文件的内容为数据，目录文件的内容为目录项或文件名与节点对应表，设备文件不占用磁盘空间，通过其节点信息可建立与内核驱动程序的联系。

8.综述Linux系统的文件权限及其管理。  
答：Linux用文件存取控制表来解决存取权限的控制问题。存取控制表以文件为单位，把用户按某种关系画分为若干组，同时规定每组用户的存取权限。每个文件都有一张存取控制表。在实现时，该表存放在文件说明中，也就是i节点的文件权限项。 就某个文件而言，它只对三类用户（文件主，同组人，其它人）分配权限。权限的修改或分配可通过命令chmod来实现。当然chmod和chgrp等命令也有着权限控制作用，因为文件的主和组变了，它相应的权限也会随之改变。

9. GNU make的工作过程是怎么样的？  
   答：1. 依次读取变量“MAKEFILES”定义的makefile文件列表
10. 读取工作目录下的makefile文件（根据命名的查找顺序“GNUmakefile”，“makefile”，“Makefile”，首先找到那个就读取那个）
11. 依次读取工作目录makefile文件中使用指示符“include”包含的文件
12. 查找重建所有已读取的makefile文件的规则（如果存在一个目标是当前读取的某一个makefile文件，则执行此规则重建此makefile文件，完成以后从第一步开始重新执行）
13. 初始化变量值并展开那些需要立即展开的变量和函数并根据预设条件确定执行分支
14. 根据“终极目标”以及其他目标的依赖关系建立依赖关系链表
15. 执行除“终极目标”以外的所有的目标的规则（规则中如果依赖文件中任一个文件的时间戳比目标文件新，则使用规则所定义的命令重建目标文件）
16. 执行“终极目标”所在的规则
17. Gcc编译过程阶段及各阶段主要工作？  
    答：预处理：生成预编译文件 编译：生成汇编文件  
    汇编：生成目标文件 链接：生成可执行文件

四、操作题

1. 简述在虚拟机中安装Red Hat Linux 9.0 的过程  
   答：  
   下载操作系统的镜像ISO文件  
   下载虚拟机并安装  
   通过ISO文件安装操作系统  
   执行相关配置即可
2. 假设你的用户账号是zheng，现在你登录进入linux系统，查看当前登录到系统中的用户,查看当前系统中运行的进程，然后再退出系统。  
   答：  
   login：zheng  
   Password：口令  
   $who  
   $ps  
   $Ctrl+D
3. 在当前目录/home/test下新建一个目录look，将当前目录改为look，在look下新建3个长度为0的文件test1、test2、test3，然后把test1移到其父目录中并改名为file1。  
   答：  
   $mkdir look  
   $ cd look  
   $ touch test1 test2 test3  
   $ mv test1 …/file1
4. 现在需要统计当前目录 /home/zheng下普通文件的数目并显示结果,如何实现？  
   答：  
   $find –type f | wc –l
5. 假设你是系统管理员，需要增加一个新的用户账号 zheng，为新用户设置初始密码，锁定用户账号 uly，并删除用户账号chang。  
   答：  
   #useradd zheng  
   #passwd  zheng  
   #passwd –l uly  
   #userdel chang
6. 若给需要将 /home/zheng 目录下的所有文件打包压缩成 /tmp/zheng.tar.gz ，你准备怎么做？当需要从压缩包中恢复时，又该如何处理？  
   答：  
   #tar –zcvf  /tmp/zheng.tar.gz  /home/zheng  
   #tar -zxvf /tmp/zheng.tar.gz
7. 根据要求编写Makefile文件,有5个文件分别是main.c、visit.h、study.h、visit.c、study.c  
   答：  
   main:main.o visit.o study.o  
   gcc main.o visit.o study.o -o main  
   main.o:main.c visit.h study.h  
   gcc -c main.c -o main.o  
   visit.o:visit.c visit.h  
   gcc -c visit.c -o visit.o  
   study.o:study.c study.h  
   gcc -c study.c -o study.o  
   clean:  
   rm -rf \*.o main
8. 建立新用户newstudent ，设置密码123456，给用户密码加锁。  
   useradd newstudent  
   passwd newstudent  
   usermod -L newstudent
9. 在当前目录中新建文件text并设置文件的属性为文件属主(u)增加执行权限与文件属主同组用户(g)增加写权限其他用户(o) 删除读权限。  
   touch text  
   chmod u+x text  
   chmod g+w text  
   chmod o-r text

三、  
58. Linux 是一种免费的完全的多任务操作系统，它完全运行在微处理器的保护模式下。 Linux 完全兼容 POSIX.1 标准。 ®  
59. 自由软件是指由开发者提供软件全部源代码并放弃包括版权在内的任何权利， 任何用户都有权使用、拷 贝、扩散、修改的软件，只要用户也将自己修改过的程序代码公开就行。 (W)  
60. Linux 是 Unix 的一个变种， 是对 Unix 内核的修补，但它可以被免费使用。 (W)  
61. Linux 版本号分为两类： 内核版本与发行版本。而 Linux 内核的版本又被分为两种： 测试版本与产品化版 本。Linux 内核版本号由三位数字组成， 其中第二位数字说明版本类型， 如果该数字是偶数， 则说明这种版

本是产品化版本；如果是奇数，则为测试版本。 ®  
62. X Window 系统是 Unix 上的标准图形界面， 是一个支持多种应用程序的环境。 Linux 用的 X Window 版本 通常是 XFree86 。®  
63. tar 命令只能进行打包或解包操作， 没有压缩功能， 用户要进行压缩操作， 必须使用其它诸如 gzip 之类的 压缩软件。 (W)

五、填充题  
64. 在 Linux 中 ， 若 要 为 命 令 ―ls -art‖ 设 置 一 个 别 名 tdir ， 则 应 命 令 行 中 键 入 别 名 命 令 ： \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ 。从命令行设置的别名只在当前会话中有效。为想在登录时使别名有效，如果 你使用的是 bash，则把这个别名定义放在用户主目录中的\_\_\_\_\_\_\_\_\_文件或\_\_\_\_\_\_\_\_\_\_\_\_文件中。(alias tdir=“ls -art”,.bashrc,.bash\_profile)

65. 在 Linux 中，用户可通过 cat 命令来创建一个新文件。若要创建新文件 abc，则应在命令行中键入 \_\_\_\_\_\_\_\_\_\_\_\_命令。然后， 用户可通过键盘键入文件内容， 输入完后按回车键， 然后按\_\_\_\_\_\_\_\_\_组合键或 \_\_\_\_\_\_\_\_\_组合键来结束输入过程即可。另外，用户还可以通过 cp 命令来创建一个新文件。若一个位于第 一 个 虚 拟 终 端 号 上 的 用 户 要 通 过 cp 命 令 创 建 新 文 件 abc ， 则 你 需 在 命 令 行 上 键 入 \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_命令。 (cat >abc ，Ctrl+d ，Ctrl+c ，cp /dev/tty1 abc)
66. 在 Linux 中，用户可通过\_\_\_\_命令来创建文件链接。链接有两种，一种被称为\_\_\_\_\_\_\_(这类链接也通常 被称为一般链接)，它要求链接文件和被链接文件必须位于同一个文件系统中， 并且不能链接目录。另一种 被称为\_\_\_\_\_\_\_\_\_\_\_\_ 的链接方式则不存在这一问题。 (ln，硬链接，符号链接)
67. 要求在 Linux 中将当前目录中的 Finished 子目录及子目录中所有文件通过 rm 命令来删除。则应键入命 令\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ 。(rm -r Finished)

六、选择填充

69. 在 Linux 中，可使用\_\_\_\_\_命令来删除指定目录。但它要求一个目录被删除之前必须是空的。而另一删除 命令\_\_\_\_\_则无此限制。操作者应是于\_\_\_\_有写权限的所有使用者。删除某目录时也必须具有对\_\_\_\_ 的写权 限。 (B ，A，C ，D)  
    A. rm  
    B. rmdir  
    C. 当前目录  
    D. 父目录  
    E. 根目录  
    F. 用户主目录
70. 在 Linux 中，被称之为\_\_\_\_链接的实际上根本不是文件，它们只是指向同一索引节点的那些目录条目。 显然，这种链接\_\_\_\_跨越设备界线，因为所有的目录条目都指向同一个索引节点。而另一种链接，被称为 ****的这种链接的目录条目包含一个文件的索引节点(该索引节点本身又是对 Linux 逻辑文件系统上某处的 另一个文件的引用)，这类链接\_\_\_\_指向同一磁盘或另一磁盘上的另一个文件或目录， ****指向另一台计算 机上的一个文件或目录。使用****，每个链接都有同等的地位(也就是说， 系统把每个链接都看作是原始文 件)，并且在文件的最后一个链接被删除之前，实际的数据不会被删除；使用**** ，当原始文件被删除时， 所有对该文件的链接也都被删除。 **(A，F ，C ，E ，E ，A，C)**  
    A. 普通链接  
    B. 索引链接  
    C. 符号链接  
    D. 指针链接  
    E. 可以  
    F. 不可以
71. 在 Linux 中， 通常对软盘使用之前要进行低级格式化(命令是\_\_\_\_\_\_\_\_\_\_)，对硬盘则要进行分区操作(通常命令有\_\_\_\_\_\_\_\_、*******等)，然后还要创建文件系统(命令是*******\_\_\_\_\_)，而要真正使用， 还需要进行挂装文件系统操作(命令是\_\_\_\_\_\_\_\_\_\_)。最后操作完成后，还应进行文件系统的卸载操作(命令是  
    \_\_\_\_\_\_\_\_\_\_)。

(B,C 或 E,E 或 C,D,G,J)  
A. format  
B. fdformat  
C. fdisk  
D. mkfs  
E. fips  
F. makefs  
G. mount  
H. setup  
I. unmount  
J. umount  
K. undelete

4. 在 Linux bash 环境中，执行 echo KaTeX parse error: Expected group after '\_' at position 13: SHELL 的执行结果是\_̲\_\_\_\_\_\_\_\_\_；执行 ec…SHELL"的执行结果是 \_\_\_\_\_\_\_\_\_\_\_ ；执行 echo '$SHELL’的执行结果是\_\_\_\_\_\_\_\_\_\_\_\_\_\_ 。(A,A,B)  
   A. /bin/bash  
   B. SHELLC.SHELLD."SHELL
   C. SHELL
   D. "SHELLC.SHELLD."SHELL"  
   E. ‘$shell’

在 Linux 中 有 一 文 件 列 表 内 容 格 式 如 下 ：  
63 lrwxrwxrwx 1 hawkeye users 6 Jul 18 09:41 nurse2 -> nurse1

问 题 一 ： 要 完 整 显 示 如 上 文 件 列 表 信 息 ， 应 该 使 用 什 么 命 令 。 请 写 出 完 整 的 命 令 行 。

问 题 二 ： 上 述 文 件 列 表 内 容 的 第 一 列 内 容 ―63‖ 是 什 么 含 义 ？

问题三：上述文件列表内容的第二列内容―lrwxrwxrwx‖中的―l‖是什么含义？对于其它类型的文件或目录等 还 可 能 会 出 现 什 么 字 符 ， 它 们 分 别 表 示 什 么 含 义 ？

问题四：上述文件列表内容的第二列内容―lrwxrwxrwx‖中的第一、二、三个―rwx‖分别代表什么含义？其中 的 ―r‖ 、 ―w‖ 、 ―x‖ 分 别 表 示 什 么 含 义 ？

问 题 五 ： 上 述 文 件 列 表 内 容 的 第 三 列 内 容 ―1‖ 是 什 么 含 义 ？

问 题 六 ： 上 述 文 件 列 表 内 容 的 第 四 列 内 容 ―hawkeye‖ 是 什 么 含 义 ？

问 题 七 ： 上 述 文 件 列 表 内 容 的 第 五 列 内 容 ―users‖ 是 什 么 含 义 ？

问 题 八 ： 上 述 文 件 列 表 内 容 的 第 六 列 内 容 ―6‖ 是 什 么 含 义 ？

问 题 九 ： 上 述 文 件 列 表 内 容 中 的 ―Jul 18 09:41‖ 是 什 么 含 义 ？

问题十：上述文件列表内容的最后一列内容―nurse2>nurse1‖是什么含义？

问题一 ls –il nurse2  
问题二 为文件 nurse2的索引节点号  
问 题 三 表示文件类型，该文件为符号链接文件 其他文件类型有：-普通文件 d 目录 b 特殊块文件 c 特殊字符文件  
问 题 四 分别表示对文件 nurse2的所有者、同组成员、其他人员都具有读/写/执行权限 r/w/x 分别表示读/写/执行权限  
问题五 表示文件 nurse2的链接数  
问题六 表示文件 nurse2的所有者  
问题七 表示文件 nurse2的属组  
问题八 表示文件 nurse2的字节数  
问题九 表示文件 nurse2被创建的日期和时间  
问题十 表示 nurse2文件被符号链接到 nurse1文件

太 多 了 , 就 做 填 空 和 选 择 了

1 hda2 表 示 （ D ）  
A IDE0 接口上的从盘 B IDE0 接口上的第二个逻辑盘 C 接口上主盘的第二个分区 D IDE0 接口上的第二 个分区

2 、 安 装 Linux 系 统 对 磁 盘 分 区 的 要 求 是 （ B ）  
A 至少有一个磁盘分区 **B 至少有两个磁盘分区** C 至少有三个磁盘分区 D 至少有四个磁盘分区 ( 根 分 区 和 交 换 分 区 )

3、系统引导的过程一般包括如下几步：1 MBR 中的引导装载程序启动；2 用户登录 3 Linux 内核运行 4 系 统 自 检 ， 正 确 的 顺 序 是 （ 1432 ）

4 、 系 统 面 板 属 于 （ B）  
A 角 落 面 板 **B 边 缘 面 板** C 浮 动 面 板 D 滑 动 面 板

5、X window 由 X 服务器、X 客户机和 X 协议组成，控制屏幕和键盘的工作由（D ）承担。  
A X 服 务 器 和 X 客 户 机 B X 服 务 器 和 X 协 议 C X 客 户 机 **D X 服 务 器**

6 、 为 执 行 前 一 个 命 令 可 使 用 以 下 （ B ） 命 令 A ! B !! C !l D ^^

7 、 关 于 Shell 的 说 法 ， 不 正 确 的 是 （ D ）  
A 操作系统外壳 B 用户与 Linux 内核之间的接口程序 C 一个命令语言解释器 D 一种和 C 类似的程序语 言 (C 是编译性的 ,shell 是解释性的 )

8 、关闭 X window 图 形 化 用 户 界 面 的 组 合 键 是 （ A ）  
**A ctrl+alt+backspace** B ctrl+alt+space C ctrl+shift+backspace D ctrl+shift+space

9 、 Pwd 命 令 的 功 能 是 （ D ）  
A 设置用户的口令 B 显示用户的口令 C 相当于 Windows 命令行里输入 CD 命令  
**D 相当于在 windows  
命令行里输入 dir 命 令**

10 、 cd 命 令 可 以 改 变 用 户 的 当 前 目 录 ， 当 用 户 键 入 cd 并 按 enter 后 （ B ）  
A 当 前 目 录 为 根 目 录  
B 当 前 目 录 没 变 ， 屏 幕 显 示 当 前 目 录  
**C 当前目录改为用户主目录**  
D 当 前 目 录 改 为 上 一 级 目 录 (C 命令是 cd ~)

11 、 Linux 系统中 进 程 优 先 级 的 取 值 范 围 是 （ A ）  
A 、 -20~19 B 、 20~-19 C 、 -19~20 D 、 19~-20 ( 其 中 -20 优 先 级 最 高 )

12 、 进 程 调 度 命 令 at 和 batch 的唯一区别是运行时间，那么 batch 是在（ B ） 运 行 。  
A 、 系 统 空 闲 时 **B 、 指 定 时 间** C 、 在 需 要 时 D 、 系 统 忙 时

14 、 当 一 个 目 录 作 为 一 个 挂 载 点 被 使 用 后 ， 该 目 录 上 的 原 文 件 （ B ） A 、 被 永 久 删 除 **B 、被隐藏，待挂载设备卸载后恢复** B 、 被 放 入 回 收 站 D 、 被 隐 藏 ， 待 计 算 机 重 新 启 动 后 恢 复

15 、 Rethat 默认的 文 件 系 统 为 （ C ）  
A 、 vfat B 、 auto **C 、 ext3** D 、 iso9600

16 、 执 行 命 令 ―chmod o+rw myfile‖ 后 ， myfile 文 件 的 权 限 变 化 为 （ B ）  
A 、 同 组 用 户 可 读 写 myfile 文 件 **B 、 其 他 用 户 可 读 写 myfile 文 件** B 、 所 有 用 户 都 可 读 写 myfile 文 件 D 、 文 件 所 有 者 读 写 myfile 文 件

17 、 Linux 中 与 Windows 系统中 Program Files 文件夹功能相类似的目录是（ D ）  
A 、 /var B 、 /home C 、 /proc **D 、 /usr**

18 、 tar 命 令 可 以 进 行 文 件 的 （ A ）  
**A 、压缩、归档和解压缩** B 、 压 缩 和 解 压 缩 C 、 压 缩 和 归 档 D 、 归 档和解压缩

19 、 负 责 执 行 防 火 墙 规 则 的 服 务 （ 守 护 进 程 ） 是 （ A ）  
**A 、 iptables** B 、 network C 、 security D 、 xinetd

20 、 eth0 设 备 的 别 名 可 为 （ B ）  
A 、 eth0-1 **B 、 eth0:0**

C 、 eth1 D 、 eth-alias

21 、 ― 网络配置 ‖ 窗 口 的 ― 主 机 ‖ 选 项 卡 中 设 置 的 内 容 将 保 存 到 （ C） 文 件 。  
A 、 /etc/hosts.conf B 、 /etc/resolv.conf **C 、 /etc/hosts** D 、 /etc/hostname

22 、 Samba 服 务 器 的 默 认 安 全 级 别 是 （ B ）  
A 、 share **B 、 user** C 、 server D 、 domain

23 、 Samba 的 核 心 是 两 个 后 台 进 程 ， 它 们 是 （ A ） 和 （ B ）  
**A 、 smbd B 、 nmbd** C 、 inetd D 、 httpd

填 空  
1 、 从图形化用户界面切换到第 3 个 虚 拟 终 端 ， 使 用 组 合 键 **alt+f3+ (Ctrl)**

2 、 修 改 (/etc/grub.conf) 文件可以改变 图 形 化 用 户 界 面 的 启 动 方 式 。

3、 Linux 中所有用户的信息保存于(/etc/passwd )和(/etc/shadow )文件，用户组信息保存在( /etc/group )和  
(/etc/gshadow ) 文 件 中 。

4 、 Linux 把用户分成 3 类 ： ( 超级用户 ) 、 系 统 用 户 和 普 通 用 户 \_ 。

5、 利用 ps 命令察看进程时，主要输出项 PID 表示(进程 ID 号)、TTY 表示(控制台终端号)。

6 、 top 命 令 可 以 动 态 的 监 视 系 统 的 运 行 状 态 ， 默 认 (5) 秒钟刷新。

7 、 超 级 用 户 和 ( 系 统 用 户 ) 可 以 修 改 进 程 的 优 先 级 。

8 、 Linux 系 统 中 默 认 的 软 盘 挂 载 点 是 (/mnt) ， 挂 载 时 的 默 认 文 件 系 统 类 型 分 别 为 (ext3) 。

9、 某文件的访问权限用数字法表示 567，用字母法则表示为 (r-xrw-rwx)。

百度的题  
1、Linux 最 早 是 由 一 位 名 叫 ( ) 的 计 算 机 爱 好 者 开 发 .  
（A）Linux Sarwar （B） Rob Pike (**C) Linus Torvalds** (D) Richard Petersen

2、下 列 ( ) 是 自 由 软 件 。  
(A) Windows XP (B) UNIX © Solaris **(D) Linux**

3、下 列 ( ) 不 是 Linux 的特点  
(A) 单用户 (B) 设备独立性 （C） 开放性 （D） 多任务

4、Linux 安 装 过 程 中 的 硬 盘 分 区 工 具 是 ( ) 。  
**（ A ） FIPS** （ B ） PQmagic （ C ） FDISK （ D ） Disk Druid

5 、 Linux 的 根 分 区 的 文 件 系 统 类 型 是 ( ) 。  
（ A ） FAT32 （ B ） ext3 （ C ） FAT16 **（ D ） NTFS**

7 、 GRUB 的菜单定义在 ( ) 文件中。  
（ A ） menu.lst （ B ） lilo.conf （ C ） httpd.conf （ D ） vsftpd.conf

8 、 在 bash 中 超 级 用 户 的 提 示 符 是 ( ) 。  
（A） # （B） C:> （C） grub> **（D） $**

9、GRUB 的命令行模式的命令提示符是 ( ) 。  
（ A ） grub> （ B ） $ （ C ） # （ D ） C:>

10 、 当 安 装 好 Linux 后 ， 系 统 默 认 的 帐 号 是 ( ) 。  
（ A ） administrator （ B ） guest **（ C ） root** （ D ） boot

11 、 在 命 令 行 模 式 中 、 输 入 ( ) 不 能 进 入 末 行 模 式 。  
（ A ） ？ （ B ） / （ C ） ： （ D ） i

12 、可以为文件或目录重命名的命令是 ( ) 。  
（ A ） rm （ B ） mv （ C ） rmdir （ **D ） mkdir**

13 、 用 于 文 件 系 统 挂 载 的 命 令 是 ( ) 。  
（ A ） mount （ B ） fdisk （ C ） df **（ D ） man**

14 、 不 能 用 来 关 机 的 命 令 是 ( ) 。  
（ A ） shutdown **（ B ） halt** （ C ） init （ D ） logout

15 、 Linux 系 统 中 ， 将 加 密 过 的 密 码 放 到 ( ) 文件中。  
（ A ） other （ B ） /etc/password **（ C ） /etc/shadow** （ D ） /etc/passwd

16 、 变 更 用 户 身 份 的 命 令 是 ( ) 。  
（ A ） who （ B ） whoami **（ C ） su** （ D ） id

17 、用于 终 止 某 一 进 程 执 行 的 命 令 是 ( ) 。  
（ A ） free （ B ） pstree **（ C ） kill** （ D ） ps

18 、比较文件的差异要用到的命令是 ( ) 。  
**（ A ） diff** （ B ） cat （ C ） wc （ D ） head

19 、 能 用 来 关 机 的 命 令 是 ( ) 。  
（ A ） login （ B ） reboot **（ C ） init** （ D ） runlevel

20 、 不 是 shell 具 有 的 功 能 和 特 点 的 是 ( ) 。  
输入输出重定向 (B) 管 道 **© 处理程序命令** （ D ） 执 行 后 台 进 程

21 、使用 rpm 命 令 安 装 软 件 包 时 、 所 用 的 选 项 是 ( ) 。  
二 、 填 空 题  
1、\_\_\_Vim\_\_\_\_\_\_是 Vi 的增强版。

2、Linux 的版本分为：********内核版本\_\_\_\_\_\_\_和\_\_\_\_\_发行版版本********\_\_\_。

3、CD-ROM 标 准 的 文 件 系 统 类 型 是 \_\_\_\_\_ ISO 9660\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ 。

4 、安装 Linux 时 最 少 需 要 两 个 分 区 ， 分 别 是 **根分区**\_\_ 和 ***交换分区***\_\_\_\_ 。

5 、 Linux 默 认 的 系 统 管 理 员 账 号 是 *****root*****\_\_\_\_ 。

6 、 命 令 接 口 演 化 为 两 种 主 要 形 式 ， 分 别 是 \_\_\_\_命令行界面（CLI）

\_\_\_\_\_ 和 ***图形用户界面（GUI）。***\_\_\_\_ 。

7 、 Red Hat Linux9.0 自 带 的 引 导 工 具 是 \_\_ GRUB（GRand Unified Bootloader） 。\_\_\_\_\_\_\_ 和 ***和 LILO（Linux Loader）***\_\_\_\_\_\_ 。

8 、 GRUB 的 用 户 界 面 有 三 种 :\_\_\_\_菜单模式、\_\_\_**命令行模式** 、 \_\_\_\_\_\_\_\_\_\_\_ 和 末 行 模 式 。

9 、 GRUB 的 默 认 菜 单 文 件 menu.lst 其 实 是 ***grub.conf***\_\_\_\_\_ 文 件 的 符 号 链 接 。

10 、 操 作 系 统 为 用 户 提 供 了 两 种 接 口 ， 分 别 是 ***命令接口***\_\_\_ 和 **程序接口**\_\_\_\_\_\_ 。

11 、 在 命 令 行 模 式 中 ， 要 进 入 GUI ，可执行 ****startx****\_\_\_ 命令。

12 、 建 立 用 户 帐 号 的 命 令 是 \_\_\_\_useradd \_\_\_\_\_\_\_\_\_ 。

13 、 设 定 帐 号 密 码 的 命 令 是 ***passwd***\_\_\_\_\_\_\_ 。

14 、 创 建 一 个 新 组 的 命 令 是 ****passwd****\_\_\_\_\_ 。

15 、 chmod 命 令 的 功 能 是 \_\_\_\_\_ 修改文件或目录的权限。\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ 。

16 、 chown 命 令 的 功 能 是 *****修改文件或目录的所有者和所属组。*****\_\_\_\_\_\_\_\_\_\_\_\_ 。

17 、查看系统信息的命令是 \_\_\_\_\_ uname -a\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ 。

18 、使用 tar 命 令 时 ， 应 该 记 住 的 两 个 选 项 组 合 是 :****-cvf \_\_\_\_\_ 和 \_\_\_\_\_ -xvf****\_\_ ，  
它 们 的 功 能 分 别 是 ： ****创建归档文件****\_\_\_\_\_ 和 *****解压归档文件*****\_\_\_ 。

19 、 gzip 命令的功能是 ****文件进行压缩或解压缩****\_\_\_\_\_\_ 。

20 、 一 个 典 型 的 KDE 桌 面 环 境 主 要 包 括 两 大 部 分 ： ***KWin 窗口管理器 \_\_\_\_\_\_\_\_ 和 \_\_\_\_ Plasma 桌面系统***\_\_\_ 。

21 、用于复制文件或目录的命令是 ****cp****\_\_\_ 。  
三 . 简答题  
1 、 简 述 Linux 的 主 要 特 点 ？  
答：

> 开源免费：Linux 的源代码公开，遵循开源许可协议，任何人可自由使用、修改和分发，降低了使用成本，吸引全球开发者共同完善。  
> 多用户多任务：支持多个用户同时登录系统，每个用户可同时执行多个任务，通过资源管理和调度机制保证各用户和任务的独立性与高效运行。  
> 良好的兼容性：能兼容多种硬件平台，可在不同架构的计算机上运行，还能支持大量的软件和文件格式。  
> 高度的稳定性：经过严格测试和优化，可长时间稳定运行，适合作为服务器操作系统，减少因系统崩溃带来的损失。  
> 强大的网络功能：内置了丰富的网络协议和工具，可轻松搭建各种网络服务，如 Web 服务器、FTP 服务器、邮件服务器等。  
> 安全可靠：提供了完善的用户权限管理、文件系统保护和防火墙等安全机制，有效防止非法入侵和数据泄露。  
> 丰富的软件资源：拥有庞大的开源软件库，涵盖了操作系统、办公软件、开发工具、多媒体软件等各个领域，可满足不同用户的需求。

2、Linux 有 哪 些 启 动 方 式 ？  
答：

> 正常启动：这是最常见的启动方式，通过 BIOS 或 UEFI 引导系统，加载内核和初始化系统服务，最终进入用户登录界面。  
> 单用户模式启动：以单用户模式启动时，系统仅加载必要的服务，用户可以以 root 身份登录，用于系统维护、修复文件系统、重置密码等操作。通常在启动时通过修改 GRUB 菜单选择单用户模式。  
> 救援模式启动：当系统无法正常启动时，可以使用救援模式。救援模式会加载一个基本的系统环境，允许用户挂载硬盘、修复文件系统、备份数据等。一般通过安装光盘或 USB 启动盘进入救援模式。

3、管 道 的 作 用 是 什 么 ？  
答：

> 管道（|）是 Linux 中一种重要的通信机制，它的作用是将一个命令的输出作为另一个命令的输入。通过管道可以将多个简单的命令组合成一个复杂的命令，实现数据的流式处理，避免了中间文件的创建和存储，提高了处理效率。例如，ls -l | grep “.txt” 命令将 ls -l 命令的输出作为 grep “.txt” 命令的输入，从而筛选出当前目录下所有以 .txt 结尾的文件信息。

4、简 述 标 准 的 Linux 运 行 级 ？  
答：

> Linux 运行级是系统的不同运行状态，不同的运行级对应着不同的系统服务和功能。标准的 Linux 运行级通常有以下几种：  
> 运行级 0：关机状态，系统将停止所有服务并关闭电源。  
> 运行级 1：单用户模式，仅加载必要的服务，用于系统维护和修复。  
> 运行级 2：多用户模式，但没有网络服务。  
> 运行级 3：多用户模式，支持网络服务，通常用于服务器环境。  
> 运行级 4：用户自定义运行级，未被系统默认使用。  
> 运行级 5：图形化界面的多用户模式，适合普通桌面用户。  
> 运行级 6：重启状态，系统将重新启动。

5、GRUB 是 什 么 ， 它 有 什 么 作 用 ？  
答：

> GRUB（Grand Unified Bootloader）是 Linux 系统中常用的引导加载程序。它的作用是在计算机启动时，负责加载操作系统内核并将控制权交给内核。具体来说，GRUB 具有以下功能：  
> 多重引导支持：可以引导多种操作系统，如 Linux、Windows 等，用户可以在启动时选择要启动的操作系统。  
> 配置灵活：用户可以通过编辑 GRUB 配置文件来定制启动选项，如修改内核参数、设置启动等待时间等。  
> 故障恢复：在系统出现故障无法正常启动时，GRUB 可以提供一些恢复选项，帮助用户修复系统。

6、、 什 么 是 Shell ， 它 的 作 用 是 什 么 ？  
答：

> Shell 是用户与 Linux 内核之间的接口程序，它接收用户输入的命令，并将其解释为内核可以理解的指令，然后传递给内核执行，最后将执行结果返回给用户。Shell 的作用主要有以下几点：  
> 命令解释：将用户输入的文本命令转换为内核可以执行的操作。  
> 脚本编程：支持编写 Shell 脚本，实现自动化任务，提高工作效率。  
> 环境管理：可以设置和管理用户的工作环境，如环境变量、别名等。

7、、 简 述 Swap 分 区 的 作 用 ？  
答：

> Swap 分区也称为交换分区，是 Linux 系统中用于扩展物理内存的一块磁盘空间。当系统的物理内存不足时，操作系统会将一些不常用的内存页面交换到 Swap 分区中，从而释放物理内存供其他程序使用。当需要访问这些被交换出去的页面时，再将其从 Swap 分区交换回物理内存。Swap 分区的作用主要是在物理内存不足时提供额外的虚拟内存，保证系统的正常运行，但由于磁盘读写速度远低于内存，过多使用 Swap 分区会导致系统性能下降。

8、简 述 vsftp 默 认 配 置 （ 匿 名 用 户 的 权 限 、 普 通 用 户 的 权 限 、 root 用 户 的 权 限 ） ？ 。  
答：

> 匿名用户权限：默认情况下，匿名用户可以登录 vsftp 服务器，具有下载文件的权限，但没有上传、删除和创建文件的权限。匿名用户的主目录通常是 /var/ftp。  
> 普通用户权限：普通用户可以使用自己的用户名和密码登录 vsftp 服务器，具有对自己主目录下文件的读写权限。可以上传、下载、删除和创建文件。  
> root 用户权限：默认情况下，root 用户不能直接登录 vsftp 服务器，这是为了保证系统的安全性。如果需要允许 root 用户登录，需要修改 vsftp 的配置文件。

9 、 samba 服 务 器 、 apache 服 务 器 、 vsftp 服 务 器 、 DNS 服 务 器 的 功 能 ？  
答：

> samba 服务器：用于在 Linux 系统和 Windows 系统之间实现文件和打印机共享。它可以让 Linux 系统像 Windows 网络中的文件服务器一样工作，方便不同操作系统之间的资源共享。  
> apache 服务器：是一款开源的 Web 服务器软件，用于在互联网或局域网中提供 Web 服务。它可以处理 HTTP 请求，将网页文件发送给客户端浏览器，支持多种编程语言和脚本，如 PHP、Python 等。  
> vsftp 服务器：是一款常用的 FTP（文件传输协议）服务器软件，用于在网络上实现文件的上传和下载。用户可以通过 FTP 客户端连接到 vsftp 服务器，进行文件的管理操作。  
> DNS 服务器：即域名系统服务器，负责将域名解析为对应的 IP 地址。当用户在浏览器中输入域名时，DNS 服务器会查找该域名对应的 IP 地址，并将其返回给浏览器，从而实现通过域名访问网站的功能。

10、什么是正则表达式，它的作用是什么，举例说明？  
答：

> 正则表达式是一种用于描述字符串模式的工具，通过特定的字符和字符组合来定义匹配规则。它的作用主要有以下几点：  
> 字符串匹配：可以在文本中查找符合特定模式的字符串。  
> 字符串替换：将符合特定模式的字符串替换为其他字符串。  
> 字符串分割：根据特定模式将字符串分割成多个部分。

四.操作题

1、用 shell 命令查看/home 目录下的可执行文件。

```
find /home -type f -executable

```

2、改变桌面背景。

```
gsettings set org.gnome.desktop.background picture-uri 'file:///path/to/your/image.jpg'

```

3、改变 info 这个文件的权限，原先为-rw-r—r–，用 shell 命令增加可执行权限。

```
chmod +x info

```

4、选择一个磁盘分区，对其进行挂载，然后访问其中内容，之后对其卸载。

```
# 创建挂载点
mkdir /mnt/mydisk
# 挂载分区
mount /dev/sdb1 /mnt/mydisk
# 访问其中内容
ls /mnt/mydisk
# 卸载分区
umount /mnt/mydisk

```

5、选用 shell 命令建立目录，并对文件和目录进行移动、复制、删除以及改名等操作。

```
# 创建目录
mkdir mydir
# 创建文件
touch myfile.txt
# 复制文件
cp myfile.txt mydir/
# 移动文件
mv myfile.txt mydir/
# 删除文件
rm mydir/myfile.txt
# 删除目录
rm -r mydir
# 改名
mv oldname.txt newname.txt

```

6、文 件 内 容 如 下 （ 名 称 为 info.dat ） ：  
48 Dec 3BC1997 LPSX 68.00 LVX2A 138 483 Sept 5AP1996 USP 65.00 LVX2C 189 49 Oct 3ZL1998 LPSX 43.00 KVM9D 512 219 Dec 2CC1999 CAD 23.00 PLV2C 68

(1) 从 文 件 info.dat 中 抽 取 代 码 为 483 和 484 的 城 市 。  
(2)从文件 info.dat 中抽取行首不是 48 的行。

```
grep '^48[34] ' info.dat

```

```
grep -v '^48' info.dat

```

7、用 Shell 脚本实现计算 1～5 的平方。

```
#!/bin/bash
for i in {1..5}; do
    square=$((i * i))
    echo "$i 的平方是 $square"
done

```

8、用 cal 命令查看 2008 年 8 月 8 日是星期几（写出 shell 命令）。

```
cal 8 2008

```

9、选择一个文件系统，对其进行挂载，然后访问其中内容，之后对其卸载。

```
# 创建挂载点
mkdir /mnt/usb
# 挂载文件系统
mount -t ext4 /dev/sdb1 /mnt/usb
# 访问其中内容
ls /mnt/usb
# 卸载文件系统
umount /mnt/usb

```

10、使 用 rpm 命 令 安 装 软 件 包 ,(bind-9.2.1-16.i386.rpm bind-utils-9.2.1-16.i386.rpm redhat-config-bind-1.9.0-13.noarch.rpm )写出相应的 shell 命令。

```
rpm -ivh bind-9.2.1-16.i386.rpm bind-utils-9.2.1-16.i386.rpm redhat-config-bind-1.9.0-13.noarch.rpm

```

11、使用 Shell 命令对用户帐号和组群进行增加、删除等操作。

```
# 创建组
groupadd mygroup
# 创建用户并加入组
useradd -g mygroup myuser
# 设置用户密码
passwd myuser
# 删除用户
userdel -r myuser
# 删除组
groupdel mygroup

```

12、对 vi 编辑器使用的操作说明（包括建立文件、保存并退出、三种模式的切换）。

> 建立文件：在终端输入 vi filename，如果文件不存在则会创建一个新文件并进入 vi 编辑器。  
> 三种模式的切换：  
> 命令模式：启动 vi 后默认进入命令模式，在此模式下可以进行光标移动、复制、粘贴、删除等操作。  
> 插入模式：在命令模式下按 i（在光标前插入）、a（在光标后插入）、o（在当前行下一行插入新行）等键可以进入插入模式，此时可以输入文本。  
> 底行模式：在命令模式下按 : 键进入底行模式，可用于保存文件、退出编辑器等操作。  
> 保存并退出：  
> 保存并退出：在底行模式下输入 :wq 然后按回车键。  
> 不保存退出：在底行模式下输入 :q! 然后按回车键。

13、用 Shell 编程计算 2\*(3 + 4)的值，并输出结果。

```
#!/bin/bash
result=$((2 * (3 + 4)))
echo "2*(3 + 4) 的值是 $result"

```

将上述脚本保存为 calculate.sh，然后执行 chmod +x calculate.sh 赋予执行权限，最后运行 ./calculate.sh。

> “社会的物质生产力发展到一定阶段，便同它们一直在其中运动的现存生产关系或财产关系（这只是生产关系的法律用语）发生矛盾。于是这些关系便由生产力的发展形式变成生产力的桎梏。那时社会革命的时代就到来了。”—— 马克思《〈政治经济学批判〉序言》，揭示了社会基本矛盾运动和社会革命发生的根源。