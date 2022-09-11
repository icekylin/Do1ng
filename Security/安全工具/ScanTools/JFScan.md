- [Usage](#usage)
- [参数](#参数)

> 基于Masscan和Nmap的极速端口扫描和服务发现工具 <https://github.com/nullt3r/jfscan>

- 相关链接
  - <https://www.freebuf.com/articles/network/332153.html>

- 下载安装

```
git clone https://github.com/nullt3r/jfscan.git
cd jfscan
pip3 install .
```

## Usage

```
仅扫描目标端口80和443，速率为10kpps：
jfscan -p 80,443 --targets targets.txt -r 10000

扫描目标前1000个端口：
jfscan --top-ports 1000 1.1.1.1/24

指定STDIN目标并管道至Nuclei：
cat targets.txt | jfscan --top-ports 1000 -q | httpx -silent | nuclei

或者，以位置参数进行配置：
jfscan --top-ports 1000 1.1.1.1/24 -q | httpx -silent | nuclei

扫描所有指定的目标：
secho target1 | jfscan --top-ports 1000 target2 --targets targets.txt -q | httpx -silent | nuclei

使用Nmap收集目标设备的更多信息：
cat targets.txt | jfscan -p 0-65535 --nmap --nmap-options="-sV --scripts ssh-auth-methods"

以文件形式提供目标，包含目标的targets.txt文件格式如下：
http://domain.com/
domain.com
1.2.3.4
1.2.3.0/24
```

## 参数

```
Target
    --targets       扫描目标文件
    -p --ports      指定扫描端口
    -r 10000        扫描速率
Report
  -oi, --only-ips       output only IP adresses, default: all resources
  -od, --only-domains   output only domains, default: all resources
  -o OUTPUT, --output OUTPUT
                        output masscan's results to specified file
```
