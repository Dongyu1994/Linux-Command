# cat

**cat** 是 Linux 下的基本命令，通过这个命令可以用来显示文件的内容。

## 使用说明

### 语法

```
$ cat [选项][参数]
```

### 选项

```
-n或-number：有1开始对所有输出的行数编号
-b或--number-nonblank：和-n相似，只不过对于空白行不编号
-s或--squeeze-blank：当遇到有连续两行以上的空白行，就代换为一行的空白行
-A：显示不可打印字符，行尾显示“$”
-e：等价于"-vE"选项
-t：等价于"-vT"选项
```

### 参数  

```
文件列表：指定要连接的文件列表
```

### 示例

**基本使用**

```
$ cat [文件列表]
```

**实例演示**

```
[root@linux-command ~]# cat auto-fdisk.sh
#!/bin/bash

# Author: Vtrois <seaton@vtrois.com>
# Project URL: https://www.vtrois.com
# Description: Auto fdisk for SpacePack Tools
# Github URL: https://github.com/Vtrois/SpacePack
……

```

## 温馨提示

当文件较大时，文本在屏幕上迅速闪过，用户往往会看不清所显示的内容。因此，一般用 more 等命令分屏显示。为了控制滚屏，可以按 Ctrl+S 键，停止滚屏；按 Ctrl+Q 键可以恢复滚屏。按 Ctrl+C（中断）键可以终止该命令的执行，并且返回 shell 提示符状态。