- [Usage](#usage)
- [参数](#参数)

> 跨平台社区 网络 CMS 指纹识别工具 https://github.com/0x727/ObserverWard

**下载安装**

```bash
# MacOS
brew install observer_ward
# 源码手动安装
git clone https://github.com/0x727/ObserverWard
cd ObserverWard
cargo build --target x86_64-unknown-linux-musl --release --all-features
```

**相关链接**
- 官方使用说明：https://0x727.github.io/ObserverWard/
- 指纹库：https://0x727.github.io/FingerprintHub/web_fingerprint_v3.json
- 插件压缩包：https://github.com/0x727/FingerprintHub/releases/download/default/plugins.zip

## Usage

**更新指纹**
- 使用 -u 参数从指纹库中更新指纹，也可以从指纹库下载 json 文件到本地
- 如果在程序的运行目录有web_fingerprint_v3.json文件会使用运行目录下的指纹库，不会读取下面表格中系统对于的目录。
- 指纹默认保存路径
  - Windows: C:\Users\Alice\AppData\Roaming\observer_ward\web_fingerprint_v3.json
  - Linux: /home/alice/.config/observer_ward/web_fingerprint_v3.json
  - macOS: /Users/Alice/Library/Application Support/observer_ward/web_fingerprint_v3.json

**更新插件**
- 使用 --update_plugins 从指纹库下载插件压缩包到用户配置目录
- 更新会删除原来的目录并且覆盖
- 插件默认保存路径
  - Windows: C:\Users\Alice\AppData\Roaming\observer_ward\plugins
  - Linux: /home/alice/.config/observer_ward/plugins
  - macOS: /Users/Alice/Library/Application Support/observer_ward/plugins

**验证指纹是否有效**
- 使用 --verify 参数指定指纹yaml的路径，-t 指定要识别的目标，输出请求过程和结果

```
# 扫描单个目标
observer_ward -t http://example.com

# 从文件扫描目标
observer_ward -f target.txt

# 从标准输出扫描
cat target.txt| observer_ward --stdin

# 导出结果到json文件
observer_ward -t https://httpbin.org -j result.json

# 导出结果到csv文件
observer_ward -t https://httpbin.org -c result.csv

关于打开csv文件中文乱码问题，和系统环境变量有关，会导致保存文件的编码为UTF-8，Mac系统或者Linux可以使用以下命令转换导出文件编码：
iconv -f UTF-8 -t GB18030 Result.csv > Result.csv
```

## 参数

```
  -c --csv value      导出 csv 文件
     --daemin         后台运行
  -f --file value     扫描文件内 URL
  -j --json value     导出 Json 文件
     --plugins value  当参数为 default 时使用 plugins 目录
     --proxy value    使用代理请求 (ex: [http(s)|socks5(h)]://host:port)
  -s --res_api value  使用 Web Server Api 请求 (ex: 127.0.0.1:8080)
     --service        使用 nmap 的指纹识别服务 (较慢)
     --silent         静默模式输出
     --stdin          标准格式输出
  -t --target value   指定目标 URL（必选，除非使用 --stdin）
     --thread value   指定扫描线程
     --timeout value  指定超时时间
     --token value    API 身份验证
  -u --update_fingerprint    更新 Web 指纹
     --update_plugins        更新 Nuclei 插件
     --update_self           更新 Observer_ward
  -V --version               打印当前版本
     --verify value       验证指定 yaml 文件
     --webhook <WEBHOOK>     将结果发送至 WebHook 服务器 (ex: https://host:port/webhook)
```