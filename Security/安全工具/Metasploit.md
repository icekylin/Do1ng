- [下载安装](#下载安装)
- [工具使用](#工具使用)
- [相关链接](#相关链接)

## 下载安装

```
wget https://osx.metasploit.com/metasploitframework-latest.pkg
vim ~/.zshrc
添加内容：export PATH="$PATH:/opt/metasploit-framework/bin"
source ~/.zshrc
```

## 工具使用

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

## 相关链接
- [macOS 下优雅的使用 Metasploit](https://www.sqlsec.com/2019/11/macmsf.html)