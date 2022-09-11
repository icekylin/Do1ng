- [Usage](#usage)
- [基本参数](#基本参数)
- [输出格式](#输出格式)

> TCP端口扫描器 5分钟内扫描整个互联网 <https://github.com/robertdavidgraham/masscan>

**下载安装**

```bash
# MacOS
brew install masscan
# Debian/Ubuntu
apt-get install git gcc make libpcap-dev
git clone https://github.com/robertdavidgraham/masscan
cd masscan
make
```

## Usage

```
masscan x.x.x.x/24 -p80,8080-8100 --echo > test.conf
masscan x.x.x.x/24 -c test.conf --rate 1000

-p 指定端口
--echo 将当前配置输出到文件中
-c 使用配置文件
--rate 速度(每秒数据包默认为100)
--banners 获取目标应用程序的Banner信息。
```

## 基本参数

```
<ip/range> IP地址范围，有三种有效格式，1、单独的IPv4地址 2、类似"10.0.0.1-10.0.0.233"的范围地址 3、CIDR地址 类似于"0.0.0.0/0"，多个目标可以用都好隔开

-p <ports,--ports <ports>> 指定端口进行扫描

--banners 获取banner信息，支持少量的协议

--rate <packets-per-second> 指定发包的速率

-c <filename>, --conf <filename> 读取配置文件进行扫描

--echo 将当前的配置重定向到一个配置文件中

-e <ifname> , --adapter <ifname> 指定用来发包的网卡接口名称

--adapter-ip <ip-address> 指定发包的IP地址

--adapter-port <port> 指定发包的源端口

--adapter-mac <mac-address> 指定发包的源MAC地址

--router-mac <mac address> 指定网关的MAC地址

--exclude <ip/range> IP地址范围黑名单，防止masscan扫描

--excludefile <filename> 指定IP地址范围黑名单文件(忽略扫描的网段)

--includefile，-iL <filename> 读取一个范围列表进行扫描

--ping 扫描应该包含ICMP回应请求

--append-output 以附加的形式输出到文件

--iflist 列出可用的网络接口，然后退出

--retries 发送重试的次数，以1秒为间隔

--nmap 打印与nmap兼容的相关信息

--http-user-agent <user-agent> 设置user-agent字段的值

--show [open,close] 告诉要显示的端口状态，默认是显示开放端口

--noshow [open,close] 禁用端口状态显示

--pcap <filename> 将接收到的数据包以libpcap格式存储

--regress 运行回归测试，测试扫描器是否正常运行

--ttl <num> 指定传出数据包的TTL值，默认为255

--wait <seconds> 指定发送完包之后的等待时间，默认为10秒

--offline 没有实际的发包，主要用来测试开销

-sL 不执行扫描，主要是生成一个随机地址列表

--readscan <binary-files> 读取从-oB生成的二进制文件，可以转化为XML或者JSON格式.

--connection-timeout <secs> 抓取banners时指定保持TCP连接的最大秒数，默认是30秒。
```

## 输出格式

```
-oX <filespec> (XML)
-oB <filespec> (Binary)
-oG <filespec> (Grep)
-oJ <filespec> (Json)
-oL <filespec> (List)
-oU <filespec> (Unicornscan format)
```
