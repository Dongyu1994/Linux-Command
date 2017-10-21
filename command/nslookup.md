# nslookup

**nslookup** 是 Linux 下的基本命令，通过这个命令可以用来查询域名的 DNS 信息。

## 使用说明

### 语法

```
$ nslookup [选项][参数]
```

### 选项

```
-sil：不显示任何警告信息
```

### 参数

```
域名：指定要查询域名
```

### 示例

**基本使用**

```
$ nslookup [域名]
```

**实例演示**

```
[root@linux-command ~]# nslookup www.vtrois.com
Server:  10.53.216.182
Address: 10.53.216.182#53

Non-authoritative answer:
www.vtrois.com  canonical name = www.vtrois.com.cdn.dnsv1.com.
www.vtrois.com.cdn.dnsv1.com  canonical name = 514688.p23.tc.cdntip.com.
Name: 514688.p23.tc.cdntip.com
Address: 121.51.128.192
```

## 温馨提示

**nslookup** 有两种工作模式，即 交互模式 和 非交互模式。在 交互模式 下，用户可以向域名服务器查询各类主机、域名的信息，或者输出域名中的主机列表。而在 非交互模式 下，用户可以针对一个主机或域名仅仅获取特定的名称或所需信息。进入交互模式，直接输入 nslookup 命令，不加任何参数，则直接进入交互模式，此时 nslookup 会连接到默认的域名服务器（即`/etc/resolv.conf`的第一个 dns 地址）。或者输入 `nslookup -nameserver/ip`。进入非交互模式，就直接输入 `nslookup 域名` 就可以了。