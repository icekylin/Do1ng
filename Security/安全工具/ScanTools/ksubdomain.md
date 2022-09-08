- [Useage](#useage)
- [模式](#模式)
  - [验证模式](#验证模式)
  - [枚举模式](#枚举模式)
- [特性和TIPS](#特性和tips)
- [Example](#example)

> 无状态子域名爆破工具 https://github.com/boy-hack/ksubdomain

**下载安装**

需要go 1.17以上版本并安装libpcap环境，运行以下命令

`go install -v github.com/boy-hack/ksubdomain/cmd/ksubdomain@latest`

## Useage

```bash
NAME:
   KSubdomain - 无状态子域名爆破工具

USAGE:
   ksubdomain [global options] command [command options] [arguments...]

VERSION:
   1.8.6

COMMANDS:
   enum, e    枚举域名
   verify, v  验证模式
   test       测试本地网卡的最大发送速度
   help, h    Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --help, -h     show help (default: false)
   --version, -v  print the version (default: false)
```

## 模式

### 验证模式

> 提供完整的域名列表，ksubdomain负责快速获取结果

```
./ksubdomain verify -h

NAME:
   ksubdomain verify - 验证模式

USAGE:
   ksubdomain verify [command options] [arguments...]

OPTIONS:
   --filename value, -f value   验证域名文件路径
   --band value, -b value       宽带的下行速度，可以5M,5K,5G (default: "2m")
   --resolvers value, -r value  dns服务器文件路径，一行一个dns地址
   --output value, -o value     输出文件名
   --silent                     使用后屏幕将仅输出域名 (default: false)
   --retry value                重试次数,当为-1时将一直重试 (default: 3)
   --timeout value              超时时间 (default: 6)
   --stdin                      接受stdin输入 (default: false)
   --only-domain, --od          只打印域名，不显示ip (default: false)
   --not-print, --np            不打印域名结果 (default: false)
   --dns-type value             dns类型 1为a记录 2为ns记录 5为cname记录 16为txt (default: 1)
   --help, -h                   show help (default: false)
```

```
从文件读取 
./ksubdomain v -f dict.txt

从stdin读取
echo "www.hacking8.com"|./ksubdomain v --stdin

读取ns记录
echo "hacking8.com" | ./ksubdomain v --stdin --dns-type 2
```

### 枚举模式

> 只提供一级域名，指定域名字典或使用ksubdomain内置字典，枚举所有二级域名

```
./ksubdomain enum -h

NAME:
   ksubdomain enum - 枚举域名

USAGE:
   ksubdomain enum [command options] [arguments...]

OPTIONS:
   --band value, -b value          宽带的下行速度，可以5M,5K,5G (default: "2m")
   --resolvers value, -r value     dns服务器文件路径，一行一个dns地址
   --output value, -o value        输出文件名
   --silent                        使用后屏幕将仅输出域名 (default: false)
   --retry value                   重试次数,当为-1时将一直重试 (default: 3)
   --timeout value                 超时时间 (default: 6)
   --stdin                         接受stdin输入 (default: false)
   --only-domain, --od             只打印域名，不显示ip (default: false)
   --not-print, --np               不打印域名结果 (default: false)
   --dns-type value                dns类型 1为a记录 2为ns记录 5为cname记录 16为txt (default: 1)
   --domain value, -d value        爆破的域名
   --domainList value, --dl value  从文件中指定域名
   --filename value, -f value      字典路径
   --skip-wild                     跳过泛解析域名 (default: false)
   --level value, -l value         枚举几级域名，默认为2，二级域名 (default: 2)
   --level-dict value, --ld value  枚举多级域名的字典文件，当level大于2时候使用，不填则会默认
   --help, -h                      show help (default: false)
```

```
./ksubdomain e -d baidu.com

从stdin获取
echo "baidu.com"|./ksubdomain e --stdin
```

## 特性和TIPS

- 无状态爆破，有失败重发机制，速度极快
- 中文帮助，-h会看到中文帮助
- 两种模式，枚举模式和验证模式，枚举模式内置10w字典
- 将网络参数简化为了-b参数，输入你的网络下载速度如-b 5m，将会自动限制网卡发包速度。
- 可以使用./ksubdomain test来测试本地最大发包数
- 获取网卡改为了全自动并可以根据配置文件读取。
- 会有一个时时的进度条，依次显示成功/发送/队列/接收/失败/耗时 信息。
- 不同规模的数据，调整 --retry --timeout参数即可获得最优效果
- 当--retry为-1，将会一直重试直到所有成功。
- 支持爆破ns记录

## Example

**枚举单个域名输出到文件**

```
ksubdomain e -d kylin.moe -o result.txt
```

**枚举文件内所有的域名，只保留域名结果输出到文件**

```
ksubdomain e --dl domain.txt --od -o subdomain.txt 
```