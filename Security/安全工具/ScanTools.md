# ScanTools.md

- [ScanTools.md](#scantoolsmd)
  - [目录扫描](#目录扫描)
    - [dirmap](#dirmap)
    - [dirsearch](#dirsearch)
  - [端口扫描](#端口扫描)
    - [Jfscan](#jfscan)
    - [masscan](#masscan)
  - [子域名扫描](#子域名扫描)
    - [ksubdomain](#ksubdomain)
    - [oneforall](#oneforall)
  - [漏洞扫描](#漏洞扫描)
    - [nucile](#nucile)
    - [xray](#xray)
  - [指纹扫描](#指纹扫描)
    - [observer_ward](#observer_ward)
  - [模糊测试](#模糊测试)
    - [wfuzz](#wfuzz)

## 目录扫描

### dirmap

> 一个高级web目录、文件扫描工具，功能将会强于DirBuster、Dirsearch、cansina、御剑。

- 相关链接
  - Github仓库: <https://github.com/H4ckForJob/dirmap>
- 使用示例
  - Github文档: <https://github.com/H4ckForJob/dirmap>

### dirsearch

> 基于 Python 的 Web 目录扫描器

- 相关链接
  - 国光的 macOS 配置优化记录#dirsearch: <https://www.sqlsec.com/2019/12/macos.html#dirsearch>
- 使用示例
  - 使用Dirsearch探测Web目录: <https://www.cnblogs.com/qingchengzi/articles/12652232.html>

## 端口扫描

### Jfscan

> 基于Masscan和Nmap的极速端口扫描和服务发现工具 <>

- 相关链接
  - <https://github.com/nullt3r/jfscan>
- 使用示例
  - <https://www.freebuf.com/articles/network/332153.html>

### masscan

> TCP端口扫描器 5分钟内扫描整个互联网

- 相关链接
  - Github仓库: <https://github.com/robertdavidgraham/masscan>
- 使用示例
  - Masscan 最快的互联网IP端口扫描器: <https://www.cnblogs.com/hubin123/p/16517022.html>

## 子域名扫描

### ksubdomain

> 无状态子域名爆破工具

- 相关链接
  - Github仓库: <https://github.com/boy-hack/ksubdomain>
- 使用示例
  - Github仓库: <https://github.com/boy-hack/ksubdomain>

### oneforall

> 功能强大的子域收集工具

- 相关链接
  - <https://github.com/shmilylty/OneForAll>
- 使用示例

  ```bash
  python3 oneforall.py --target example.com run
  python3 oneforall.py --targets ./example.txt run
  # Linux创建软链接
  echo 'alias oneforall="python3 [OneForAll路径]/oneforall.py"' >> ~/.zshrc
  ```

## 漏洞扫描

### nucile

> 漏洞扫描，批量检测，自定义POC <https://github.com/projectdiscovery/nuclei>

- 相关链接
  - 官方使用文档: <https://nuclei.projectdiscovery.io/templating-guide/protocols/http/>
  - README_CN: <https://github.com/projectdiscovery/nuclei/blob/master/README_CN.md>
- 使用示例
  - 编写POC或使用工具批量检测: <https://www.yuque.com/moekylin/blog/ps1d2p#lklfJ>
  - Nuclei新版README翻译及用法: <https://xdym11235.com/archives/nuclei.html>

### xray

> 一款完善的安全评估工具，支持常见 web 安全问题扫描和自定义 poc

- 相关链接
  - Github仓库: <https://github.com/chaitin/xray>
- 使用示例
  - 一个 xray PoC 的编写全过程: <https://stack.chaitin.com/techblog/detail?id=55>

## 指纹扫描

### observer_ward

> 跨平台社区 网络 CMS 指纹识别工具

- 相关链接
  - Github仓库: <https://github.com/0x727/ObserverWard>
  - 指纹库：<https://0x727.github.io/FingerprintHub/web_fingerprint_v3.json>
  - 插件压缩包：<https://github.com/0x727/FingerprintHub/releases/download/default/plugins.zip>
- 使用示例
  - 官方使用说明：<https://0x727.github.io/ObserverWard/>

## 模糊测试

### wfuzz

> 基于 Python 的目录、参数、接口模糊测试工具

- 相关链接
  - Github仓库: <https://github.com/xmendez/wfuzz>
  - mac安装pycurl方案: <https://segmentfault.com/q/1010000012674778>
  - Python pip Could not fetch URL 解决方案: <https://blog.csdn.net/liulanba/article/details/115944889>
- 使用示例
  - Wfuzz详细指南|模糊测试工具使用方法: <https://www.ddosi.org/wfuzz-guide/>
  - Wfuzz初上手: <https://gh0st.cn/archives/2018-10-28/1>
