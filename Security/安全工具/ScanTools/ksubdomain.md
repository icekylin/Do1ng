
> 无状态子域名爆破工具 https://github.com/knownsec/ksubdomain

**下载安装**

下载二进制文件即可直接运行

https://github.com/knownsec/ksubdomain/releases

```bash
# Linux 创建环境变量（可选）
echo 'export PATH="$PATH:/Users/kylin/Security.localized/ScanTools/ksubdomain/"' >> ~/.zshrc
```

## 常用命令

```bash
使用内置字典爆破
ksubdomain -d seebug.org

使用字典爆破域名
ksubdomain -d seebug.org -f subdomains.dict

字典里都是域名，可使用验证模式
ksubdomain -f dns.txt -verify

爆破三级域名
ksubdomain -d seebug.org -l 2

通过管道爆破
echo "seebug.org"|ksubdomain

通过管道验证域名
echo "paper.seebug.org"|ksubdomain -verify

仅使用网络API接口获取域名
ksubdomain -d seebug.org -api

完整模式,先使用网络API，在此基础使用内置字典进行爆破
ksubdomain -d seebug.org -full
```