- [Python Basic](#python-basic)
  - [Basic statement](#basic-statement)
- [Python Module](#python-module)
  - [requests](#requests)
  - [fake_useragent](#fake_useragent)
  - [random](#random)
  - [time](#time)

## Python Basic

### Basic statement

```python
# 取消定义变量
del [var]
```

## Python Module

### requests

>向URL发送请求, requests 传输 post 数据时会默认使用 url 编码传输数据

**相关链接**

- [Python+requests 之urlencode编码与解码](https://blog.csdn.net/weixin_43507959/article/details/106578516)

```python
# 指定 Content-Type 为 json
headers = {'Content-Type': 'application/json'}
```

```python
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

>生成随机或伪造的 UserAgent 头
>
>项目仓库：<https://github.com/hellysmile/fake-useragent>

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

### random

>生成随机数

```python
# 生成 1-99 随机整数 间隔为 1
random.randrange(1,100,1)
# 从 list 中随机返回一个数
list = [36, 36.5, 37]
a = random.sample(list, 1)
type(a)
  <class 'list'>
```

### time

> 获取时间

```python
# 格式化当前时间
time.strftime("%Y%m%d-%H%M%S")
  20220101-000000 #年月日-时分秒
```
