# ls

**ls** 是 Linux 下的基本命令，通过这个命令可以用来显示目标列表，并且可以进行彩色加亮显示，用来分区不同类型的文件。

## 使用说明

### 语法

```
$ ls [选项][参数]
```

### 选项

```
-a：显示目录下的所有文件，包括以"."开头的隐含文件
-A：显示目录下的所有文件，但不列出"."和".."
-k：显示目录下的所有文件，并且文件和目录的大小以字节为单位排列
-s：显示目录下的所有文件，并以区块为单位的形式表示文件和目录的大小
-l：显示目录下的所有文件，并以详细信息显示
-F：在每一个文件的末尾加上一个字符说明该文件的类型
-t：列出目录下的所有文件，并以更改时间排序
-R：列出目录下的所有文件，并将所有子目录的文件都列出来
```

### 参数

* 目标：需要显示列表的目录名称

### 示例

**基本使用**

```
$ ls
```

**实例演示**

```
[root@linux-command /]# ls
bin   data  etc   lib    media  opt   root  sbin  sys  usr
boot  dev   home  lib64  mnt    proc  run   srv   tmp  var
```

**-a 选项使用**

```
$ ls -a
```

**实例演示**

```
[root@linux-command /]# ls -a
.   .autorelabel  boot  dev  home  lib64  mnt  proc  run   srv  tmp  var
..  bin           data  etc  lib   media  opt  root  sbin  sys  usr
```

**-A 选项使用**

```
$ ls -A
```

**实例演示**

```
[root@linux-command /]# ls -A
.autorelabel  boot  dev  home  lib64  mnt  proc  run   srv  tmp  var
bin           data  etc  lib   media  opt  root  sbin  sys  usr
```

**-k 选项使用**

```
$ ls -k
```

**实例演示**

```
[root@linux-command /]# ls -k
bin   data  etc   lib    media  opt   root  sbin  sys  usr
boot  dev   home  lib64  mnt    proc  run   srv   tmp  var
```

**-l 选项使用**

```
$ ls -l
```

**实例演示**

```
[root@linux-command /]# ls -l
total 48
lrwxrwxrwx.  1 root root    7 Jun 11 19:47 bin -> usr/bin
dr-xr-xr-x.  4 root root 4096 Jul 25 11:54 boot
drwxr-xr-x   2 root root 4096 Aug 23 12:18 data
drwxr-xr-x  18 root root 2940 Aug 23 11:58 dev
drwxr-xr-x. 85 root root 4096 Aug 23 11:58 etc
drwxr-xr-x.  2 root root 4096 Nov  5  2016 home
lrwxrwxrwx.  1 root root    7 Jun 11 19:47 lib -> usr/lib
lrwxrwxrwx.  1 root root    9 Jun 11 19:47 lib64 -> usr/lib64
drwxr-xr-x.  2 root root 4096 Nov  5  2016 media
drwxr-xr-x.  2 root root 4096 Nov  5  2016 mnt
drwxr-xr-x.  3 root root 4096 Jun 11 19:52 opt
dr-xr-xr-x  86 root root    0 Aug 23 11:58 proc
dr-xr-x---.  5 root root 4096 Aug 23 11:59 root
drwxr-xr-x  22 root root  740 Aug 23 11:59 run
lrwxrwxrwx.  1 root root    8 Jun 11 19:47 sbin -> usr/sbin
drwxr-xr-x.  2 root root 4096 Nov  5  2016 srv
dr-xr-xr-x  13 root root    0 Aug 23 11:58 sys
drwxrwxrwt.  7 root root 4096 Aug 23 12:00 tmp
drwxr-xr-x. 13 root root 4096 Jun 11 19:47 usr
drwxr-xr-x. 19 root root 4096 Aug 23 11:58 var
```

**-R 选项使用**

```
$ ls -R
```

**实例演示**

```
[root@linux-command ~]# ls -R
.:
ls-1  ls-2  ls-3

./ls-1:
ls-1-1  ls-1-2

./ls-1/ls-1-1:

./ls-1/ls-1-2:
ls.c

./ls-2:
ls -2-1

./ls-2/ls -2-1:

./ls-3:
```

**-F 选项使用**

```
$ ls -F
```

**实例演示**

```
[root@linux-command /]# ls -F
bin@   data/  etc/   lib@    media/  opt/   root/  sbin@  sys/  usr/
boot/  dev/   home/  lib64@  mnt/    proc/  run/   srv/   tmp/  var/
```

## 拓展选项

```
--color[=WHEN]
```

更改 **ls** 输出内容的颜色，**WHEN** 可以为'never'、'auto'、'always'

## 温馨提示

-l 选项中显示的详细信息为文件名，文件类型、权限模式、硬连接数、所有者、组、文件大小和文件的最后修改时间等

-F 选项中显示的内容解释："@"表示符号链接、"|"表示FIFOS、"/"表示目录、"="表示套接字

-a 选项中显示的内容解释："."表示当前目录，".."表示当前目录的父目录

--color[=WHEN] 参数中显示的内容解释：蓝色-->目录、绿色-->可执行文件、红色-->压缩文件、浅蓝色-->链接文件、灰色-->其他文件