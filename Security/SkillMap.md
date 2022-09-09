- [0x01 快速入门](#0x01-快速入门)
  - [Stage 0 - 前置技能](#stage-0---前置技能)
  - [Stage 1 - 靶场学习](#stage-1---靶场学习)
  - [Stage 2 - 靶机渗透](#stage-2---靶机渗透)
  - [Stage 3 - 编程能力](#stage-3---编程能力)
    - [Shell 局域网存活扫描](#shell-局域网存活扫描)
    - [Python 获取目标banner](#python-获取目标banner)
    - [Python 端口扫描](#python-端口扫描)
  - [Stage 4 - 综合能力](#stage-4---综合能力)
- [0x02 Web 安全专项学习](#0x02-web-安全专项学习)
  - [1. 信息收集](#1-信息收集)
  - [2. 逻辑漏洞](#2-逻辑漏洞)
  - [3. Web-Basic](#3-web-basic)

> 个人学习途径，仅供参考

## 0x01 快速入门

笔记不是刚需，但是当你第二次遇到同样简单的问题的时候，你还需要通过搜索引擎去查询，那不妨把简单的内容记录在笔记内，以供随时查阅参考。

因为是快速入门阶段，为快速了解体系，不会过多的深入原理。

### Stage 0 - 前置技能

"一个不会编程的运维不是一个好的黑客"

学习安全需要搭建靶场、编写脚本、读懂代码，在正式学习之前，至少需要掌握以下几种能力

- 虚拟机软件的使用（如 VMware、VirtualBox 等）
- Linux操作系统基础（文件操作、目录切换、磁盘挂载、权限管理等）
- 简单服务的搭建（Apache/Nginx、MySQL、PHP）

对于虚拟机软件 Windows 下主要推荐使用 **VMware Workstation**，界面简单容易上手。服务的搭建可以使用集成软件如：**Phpstudy**、**wampserver** 等软件，只需要能正常访问即可。Linux 操作系统建议长期使用，熟悉在命令行对文件进行增删查改的操作。在掌握 Linux 基本命令之后对服务搭建的技能进行拓展，在 Linux 上搭建一个完整 Web Server 服务，通常是使用的是 **Apache + MySQL + PHP**，简称也就是 LAMP（Linux Apache MySQL PHP）。

### Stage 1 - 靶场学习

在掌握了基本服务的搭建技能后，可以通过搭建靶场来进行综合能力的学习，常见的靶场如 DVWA、Pikachu 都是不错的综合渗透测试靶场，这里以 DVWA 为例，可以通过 Phpstudy 或者 Linux 搭建 DVWA 靶场环境，在靶场内，需要学习的技能有如下

- Brute Force 暴力破解
  - 使用 BurpSuite 利用字典进行暴力破解
- Command Injection 命令注入
  - 需要掌握 Linux、Windows 操作系统下命令行的连接符使用
- CSRF #TODO
- File Inclusion 文件包含
  - 需要对 PHP 读取文件的函数进行学习
- File Upload 文件上传
  - 需要学习如何编写一个简单的后门程序，关键词为 一句话木马，针对 PHP 搭建的服务也就是 PHP一句话木马，需要使用 蚁剑、冰蝎等工具进行连接。这里推荐使用[蚁剑](https://github.com/AntSwordProject/antSword)
- SQL Injection SQL注入
  - 需要学习 SQL 基本语句，包括注释以及查询。
- XSS
  - 需要学习 JavaScript，如何利用 `<script>` 标签弹出提示框以及 Cookie

有关于靶场的学习内容，合理的利用搜索引可以轻松的获取到答案，针对 DVWA 的安全等级机制，不需要对 Medium、High、Impossible 的利用方式了然于心，但对于 Low 等级的利用方式，需要做到可以脱离任何资料而去利用。

### Stage 2 - 靶机渗透

靶机渗透测试可以帮助你速成脚本小子，也可以让你初步了解渗透测试的基本流程，在这过程中可能会使用大量的工具辅助，以下为 DC:1 靶机作为参考的学习途径

下载地址：<https://www.vulnhub.com/entry/dc-1,292/>

1. VMware 或 VirtualBox 搭建靶机
2. 网络环境正常后进行局域网存活扫描（常用的工具有 fping、arping、nmap）`fping -aqg [网段/子网掩码]`
3. 对靶机端口信息进行扫描 `nmap -sV [Target_IP]`
4. 针对 Web 服务使用 msfconsole 可利用模块
   1. 任意文件上传，使用蚁剑连接一句话木马
   2. 缓冲区溢出，获取目标系统 Shell
5. 利用 SUID 文件提升权限

对靶机的渗透测试互联网上同样有大部分的参考实例，关键词为 靶机名称+WriteUp 或 靶机名称+Walkthrough，有过一次完整的打靶经验那我们就快速进入下一个阶段吧，不要过度迷恋这个感觉，毕竟靶机是打不完的。

TIPS：工具的安装和使用并不会一帆风顺，有时需要查阅大部分的资料，对于不同环境的搭建又各有不同，可以使用集成的渗透测试系统如：Kali、Parrot等，这里推荐 [Kali](https://www.kali.org/)

### Stage 3 - 编程能力

在愉快的脚本小子生活结束后，不要忘了巩固你的编程能力，有几门常用的语言适合作为渗透测试的辅助语言如 Python，Shell，下面推荐几个简单的项目快速理解

#### Shell 局域网存活扫描

```shell
#!/bin/bash
for i in {1..254}
  do
      (if ping -c 1 -W 1 10.110.2.$i &> /dev/null;then # 替换IP段为自身所处的IP段
          echo "10.110.2.$i is up"
      fi)&
  done
wait
```

#### Python 获取目标banner

```python
import socket
s = socket.socket()
s.connect(("198.46.152.109",22)) # 198.46.152.109 是我的 vps 地址，22对应的服务是 SSH
banner = s.recv(1024)
print(banner)
```

#### Python 端口扫描

```python
from socket import *

for port in range(1,100):
    try:
        s = socket(AF_INET,SOCK_STREAM)
        s.connect(("198.46.152.109",port)) 
        print('[+] Port:%d Open' % port)
        s.close()
    except:
        print('[-] Port:%d Close' % port)
```

编程语言的学习入门通常需要掌握数据结构，循环，错误处理。对于 Python 还需要掌握一些模块，如上面使用到的 socket、requets 等。除此之外还有一些可能会用到的语言如 Go、Java、C，因为 Python 是一门很适合编写工具的脚本语言，所以暂时不对其他语言做深入了解（当然如果你有其他方面的能力也可以直接运用在网络编程的领域）

### Stage 4 - 综合能力

在掌握基本能力以后你已经可以编写简单的脚本程序来临时代替 fping、nmap 等工具来辅助你进行渗透测试（当然这并不是刚需）

一入网安深似海，我的路线并不一定是最完美的，但既然我都可以总结出来，相信你也可以在此基础上更加精进。

从这里开始学习就变得更加需要深度和广度，如完善理解 SQL注入的原理，通过 SQLi-Labs 等靶场进一步学习，或是通过 Upload-Labs 靶场进一步学习绕过文件上传限制的方式，选择必备的技能以及感兴趣的方向，继续深度的学习，下面是两个比较完善的例子。

- [黑客街 web渗透学习路线图](https://www.hackjie.com/1500.html)
- [余弦的安全技能树简版](https://evilcos.me/security_skill_tree_basic/index.html)

---

## 0x02 Web 安全专项学习

未来的学习路线规划，To Doing

Unknow Time

- [X] DVWV - SQL注入、文件上传、文件包含、文件上传、命令执行
- [X] Upload-Lbas - 通关
- [X] Python - 端口扫描器、局域网存活扫描

### 1. 信息收集

- [X] [信息收集 2022-08-29](Web安全/信息收集.md)
  - [x] 域名信息收集
  - [x] 子域名信息收集
  - [x] 站点信息收集
  - [x] 敏感信息收集
  - [x] 相关应用搜集

### 2. 逻辑漏洞

- [ ] [逻辑漏洞](Web安全/逻辑漏洞.md)
  - [x] 密码找回 - 2022-09-07
  - [x] 越权漏洞 - 2022-09-09
  - [ ] 支付漏洞
  - [ ] 未授权访问
  - [ ] 条件竞争
  - [ ] 数据包重放
  - [ ] 参数绑定

### 3. Web-Basic

- [ ] SQLinject
- [ ] FileUpload
- [ ] XSS
- [ ] CSRF
- [ ] CORS
