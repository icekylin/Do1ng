
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [语句备忘录](#语句备忘录)
- [一些模块](#一些模块)
  - [requests](#requests)

<!-- /code_chunk_output -->

## 语句备忘录

```
# 取消定义变量
del [var]
```

## 一些模块

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