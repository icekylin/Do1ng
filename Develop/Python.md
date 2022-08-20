
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [0x01 基础语句](#0x01-基础语句)
- [0x02 模块使用](#0x02-模块使用)
  - [requests模块](#requests模块)
    - [数据传递类型](#数据传递类型)
    - [Session会话](#session会话)

<!-- /code_chunk_output -->

## 0x01 基础语句

```
# 取消定义变量
del [var]
```

## 0x02 模块使用

### requests模块

#### 数据传递类型

```
# 指定 Content-Type 为 json
headers = {'Content-Type': 'application/json'}
```

#### Session会话

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