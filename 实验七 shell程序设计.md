## 实验七 shell程序设计

### 一、实验目的

理解shell的工作原理，学会编写shell脚本。

### 二、实验内容

1.编写不同功能的脚本程序。  
2.利用chmod修改文件权限。  
3.掌握脚本文件执行的方法。

### 三、主要实验步骤

1.创建一个名为zs\_lab7的目录，下边实验步骤都在该目录下完成。  
编写 lhn2025 脚本：nano lhn2025

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/81581006fc4243a1809d58f72b24ab92.png)

2.创建一个名为zs2025的脚本，一旦运行该脚本，将清除屏幕，随后输出脚本程序功能信息，并提示和等待用户按任意键继续执行，每次执行会将当前用户名称、日期和时间追加到当前目录下的子目录AA的文件aa中（如果目录AA和文件aa不存在，则脚本应该可以检测并创建它们），每次执行完毕提示用户是否继续执行追加信息，按Y继续，按N结束脚本。

创建实验目录  
mkdir -p ~/lhn\_lab7cd ~/lhn\_lab7

编写 lhn2025 脚本

```
nano lhn2025

```

粘贴以下内容：

```
#!/bin/bash
clearecho "LHN2025 Script"read -p "Press any key to continue..."date >> ~/lhn_lab7/AA/aa.txtwhile true; do
    read -p "Continue? (Y/N): " choice
    case $choice in
        [Yy]* ) date >> ~/lhn_lab7/AA/aa.txt ;;
        [Nn]* ) exit ;;
        * ) echo "Invalid input" ;;
    esacdone

```

保存并退出（Ctrl+O, Ctrl+X）  
设置执行权限  
chmod +x lhn2025

创建测试目录和文件

```
mkdir -p AAtouch AA/aa.txt

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/35df3bc4070e4eb68f34df8350136cde.png)

3.创建一个名为zs1（你姓名拼音第一个字母的缩写，如张三的文件为zs1，下边步骤以此类推，只要是zs通通改为你本人姓名相应的形式）的脚本文件，能实现如下功能并运行该脚本。  
A.清屏。  
B.空两行，然后程序暂停15秒。  
C.显示当前系统内核版本信息、日期和时间。  
D.显示当前系统内存使用情况。  
E.让计算机发出一小会蜂鸣声。  
F.检查当前目录下是否有名为CPP的目录，若没有则创建一个。  
G.将当前目录下所有文件和目录信息保存到一个新文件zs中。  
H.白底黑字在屏幕中部位置显示信息“Hi,*Zhang-San*”。  
I.提示按任意键关闭显示属性，并输出“Bye…”。

```
lhn1 脚本关键部分
bash
#!/bin/bash
clear
sleep 15
uname -r
date
free -h
echo -e '\a'
mkdir -p CPP
ls -la > lhn.txt

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/667aa3f5a51d45319faf815ab79f7b17.png)

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ec72c21e350f497fbcdbd21dbb57d6f6.png)

4.编写zs2A脚本，使之能够计算从键盘输入的3个整数的最小值，输入前应该有信息提示，输入后应该有整数（允许整数为负数，如-3、-82等）的验证，如果输入的不是整数则要求重新输入。

```
lhn2A 脚本验证输入

while true; do
    read -p "Enter integer: " num
    if [[ $num =~ ^-?[0-9]+$ ]]; then
        break
    else
        echo "Invalid integer"
    fidone

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2cfe07209f38491fbfab58edb9015e4b.png)

5.编写zs2B脚本，使之能从命令行接收参数，比如输入命令zs2B 12 55 zebra 37，程序运行显示整数参数中最大的一个：the largest number is : 55。

lhn2B 脚本处理参数

```
max=0for arg in "$@"; do
    if [[ $arg =~ ^[0-9]+$ ]]; then
        if (( arg > max )); then
            max=$arg
        fi
    fidoneecho "Largest: $max"

```

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7e1542a241d349a897ad9d7834485c76.png)

6.利用for循环、while循环或until循环编写脚本zs3，对命令行传给它的数字参数求和并显示结果。比如输入命令zs3 10 20 30 40，那么输出结果：10+20+30+40=100，注意参数的个数不限。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/eea8a5288d594cd1b17b072247dd49e7.png)

## 四、思考题

1.在shell中，之前的课程里讲过用()编组命令，请问使用{命令1;命令2; … }和(命令1; 命令2; …)两种方式差别在哪，做实验验证下。

答：编组命令区别  
{cmd1; cmd2;} 在当前 shell 执行  
( cmd1; cmd2; ) 在子 shell 执行

验证方法：

2.系统变量∗和\*和∗和@分别代表什么含义，区别是什么？举例说明下。

答：系统变量区别  
$\* 将所有参数视为单个字符串  
@保留每个参数的独立性示例：args="ab"foriin"@ 保留每个参数的独立性
示例：
args="a b"
for i in "@保留每个参数的独立性示例：args="ab"foriin"\*“; do echo KaTeX parse error: Expected 'EOF', got '#' at position 10: i; done #̲ 输出 "a b"
for i…@”; do echo $i; done # 输出 a 和 b

```
1. 新建一个脚本文件
在终端里使用 nano 或者 vim 编辑器来创建一个新的脚本文件，就叫 test_params.sh 吧。

2. 编写脚本内容
把下面的代码复制粘贴到 test_params.sh 文件中。
bash
#!/bin/bash

```

## 设置参数

```
args="a b"

```

## 定义函数来测试 $\*

```
test_star() {
    echo "使用 \$* 的结果："
    for i in "$*"; do
        echo $i
    done
}

```

## 定义函数来测试 $@

```
test_at() {
    echo "使用 \$@ 的结果："
    for i in "$@"; do
        echo $i
    done
}

```

## 调用测试函数

```
test_star $args
test_at $args

```