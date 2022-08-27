- [Python Basic](#python-basic)
  - [Basic statement](#basic-statement)
- [Python Module](#python-module)
  - [requests](#requests)
  - [fake_useragent](#fake_useragent)

## Python Basic

### Basic statement

```
# 取消定义变量
del [var]
```

## Python Module

### requests

requests 传输 post 数据时会默认使用 url 编码传输数据

[Python+requests 之urlencode编码与解码](https://blog.csdn.net/weixin_43507959/article/details/106578516)

```
# 指定 Content-Type 为 json
headers = {'Content-Type': 'application/json'}
```

```
# 建立会话
session = requests.session()
# 返回响应头
session.herders
# 返回cookie
session.cookies
# 返回指定cookie
session.cookies["字段"]
# 关闭会话
session.close
```

### fake_useragent
- 模块归类：生成随机或伪造的 UserAgent 头
- 项目仓库：https://github.com/hellysmile/fake-useragent
```python
# 实例化
from fake_useragent import UserAgent
ua = UserAgent()
# 伪造 chrome 浏览器 UserAgent
# 其他可用的浏览器 firefox/safari/ie/opera
ua.chrome
# 随机生成 UserAgent
ua.random
```