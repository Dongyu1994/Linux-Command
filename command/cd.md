# cd

**cd** 是 Linux 下的基本命令，通过这个命令可以用来切换用户当前的工作目录。

## 使用说明

### 语法

```
$ cd [选项][参数]
```

### 选项

```
~：进入当前用户主目录
-：返回并进入此目录之前所在的目录
..：返回上级目录
```

### 示例

**基本使用**

```
$ cd [目录名称]
```

实例演示

```
[root@linux-command ~]# cd linux_cd

[root@linux-command linux_cd]#
```

**- 参数使用**

```
$ cd -
```

实例演示

```
[root@linux-command linux_cd]# cd -

/root

[root@linux-command ~]#
```

**.. 参数使用**

```
$ cd ..
```

实例演示

```
[root@linux-command ~]# cd ..

[root@linux-command /]# 
```

## 温馨提示

**cd** 命令中的目录名称可以为绝对位置，若当前位置为根目录 `/` 时，返回上级目录仍为根目录 `/` 。