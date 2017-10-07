# dig

**dig** 命令可以用来测试域名系统工作是否正常。

## 使用说明

### 语法

```
$ dig [选项][参数]
```

### 选项

```
-b<ip地址>：当主机具有多个IP地址，指定使用本机的哪个IP地址向域名服务器发送域名查询请求
-f<文件名称>：指定dig以批处理的方式运行，指定的文件中保存着需要批处理查询的DNS任务信息
-P：指定域名服务器所使用端口号
-t<类型>：指定要查询的DNS数据类型
-x<IP地址>：执行逆向域名查询
-4：使用IPv4
-6：使用IPv6
-h：显示指令帮助信息
```

### 参数

```
主机：指定要查询域名主机
查询类型：指定DNS查询的类型
查询类：指定查询DNS的class
查询选项：指定查询选项
```

### 示例

**基本使用**

```
$ dig [主机]
```

**实例演示**

```
[root@linux-command ~]# dig www.vtrois.com

; <<>> DiG 9.9.4-RedHat-9.9.4-38.el7_3.3 <<>> www.vtrois.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 12999
;; flags: qr rd ra; QUERY: 1, ANSWER: 3, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;www.vtrois.com.                        IN      A

;; ANSWER SECTION:
www.vtrois.com.         120     IN      CNAME   www.vtrois.com.cdn.dnsv1.com.
www.vtrois.com.cdn.dnsv1.com. 600 IN    CNAME   514688.p23.tc.cdntip.com.
514688.p23.tc.cdntip.com. 180   IN      A       121.51.128.192

;; Query time: 152 msec
;; SERVER: 10.53.216.182#53(10.53.216.182)
;; WHEN: Fri Nov 24 15:47:32 CST 2017
;; MSG SIZE  rcvd: 133
```