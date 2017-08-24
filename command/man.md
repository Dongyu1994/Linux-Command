# man

**man** 命令是 Linux 下的帮助命令，通过这个命令可以快速查询 Linux 中的命令帮助、配置文件帮助和编程帮助等信息，并且格式化显示。

## 使用说明

### 语法

```
$ man [选项][参数]
```

### 选项

```
-a：显示所有匹配项
-d：显示 man 查照手册文件时搜索路径信息,不显示手册页内容
-f：指定内容时使用分页程序
-h：显示帮助信息
-k：搜索 whatis 数据库，模糊查找关键字
-f：在 whatis 数据库查找以关键字开头的帮助索引信息
-w：显示找到手册文件路径，默认搜索一个文件
-M：指定 man 手册搜索的路径
```

### 参数

* 关键字：指定要搜索帮助的关键字

### 示例

**基本使用**

```
$ man cat
```

**实例演示**

```
[root@linux-command ~]# man cat
CAT(1)                           User Commands                          CAT(1)

NAME
       cat - concatenate files and print on the standard output

SYNOPSIS
       cat [OPTION]... [FILE]...

DESCRIPTION
       Concatenate FILE(s), or standard input, to standard output.

       -A, --show-all
              equivalent to -vET

       -b, --number-nonblank
              number nonempty output lines, overrides -n

       -e     equivalent to -vE

       -E, --show-ends
              display $ at end of each line

       -n, --number
 Manual page cat(1) line 1 (press h for help or q to quit)
```

**-w 选项使用**

```
$ man -w cat
```

**实例演示**

```
[root@linux-command /]# man -w cat
/usr/share/man/man1/cat.1.gz
```

## 温馨提示

在使用 **man** 命令查看帮助文件的时候，可以使用 `PageUp` 与 `PageDown` 翻页，按 `h` 键获取帮助说明，按 `q` 键退出帮助手册。