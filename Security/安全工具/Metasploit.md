# Metasploit

## 下载安装

```
# macOS 下优雅的使用 Metasploit
https://www.sqlsec.com/2019/11/macmsf.html
# 最新版下载
https://osx.metasploit.com/metasploitframework-latest.pkg
# 最新的前10个版本
https://osx.metasploit.com/
# 添加环境变量
vim ~/.zshrc
添加以下内容
export PATH="$PATH:/opt/metasploit-framework/bin"
```

## 基础命令

```
# 搜索指定模块
msf search KEYWORD
# 调用模块
msf use /PATH
# 查看参数
msf show options
# 设置参数
msf set OPTIONS VALUES
# 运行模块
msf exploit
```
