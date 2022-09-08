- [告知服务器意图的 HTTP 方法](#告知服务器意图的-http-方法)
  - [GET 获取资源](#get-获取资源)
  - [POST 传输实体主体](#post-传输实体主体)
  - [PUT 传输文件](#put-传输文件)
  - [HEAD 获得报文首部](#head-获得报文首部)
  - [DELETE 删除文件](#delete-删除文件)
  - [OPTIONS 询问请求的方法](#options-询问请求的方法)

## 告知服务器意图的 HTTP 方法

### GET 获取资源  
GET 方法用来请求访问已被 URI 识别的资源。指定的资源经服务器 端解析后返回响应内容。也就是说，如果请求的资源是文本，那就保 持原样返回;如果是像 CGI(Common Gateway Interface，通用网关接 口)那样的程序，则返回经过执行后的输出结果。

使用 GET 方法的请求/响应的例子
![](images/HTTP-1.png)

### POST 传输实体主体
POST 方法用来传输实体的主体。
虽然用 GET 方法也可以传输实体的主体，但一般不用 GET 方法进行 传输，而是用 POST 方法。虽说 POST 的功能与 GET 很相似，但 POST 的主要目的并不是获取响应的主体内容。

使用 POST 方法的请求·响应的例子
![](images/HTTP-2.png)

### PUT 传输文件
PUT 方法用来传输文件。就像 FTP 协议的文件上传一样，要求在请
求报文的主体中包含文件内容，然后保存到请求 URI 指定的位置。

但是，鉴于 HTTP/1.1 的 PUT 方法自身不带验证机制，任何人都可以 上传文件 , 存在安全性问题，因此一般的 Web 网站不使用该方法。若 配合 Web 应用程序的验证机制，或架构设计采用 REST(REpresentational State Transfer，表征状态转移)标准的同类 Web 网站，就可能会开放使用 PUT 方法。

使用 PUT 方法的请求·响应的例子
![](images/HTTP-3.png)
1 响应的意思其实是请求执行成功了，但无数据返回。

### HEAD 获得报文首部
HEAD 方法和 GET 方法一样，只是不返回报文主体部分。用于确认 URI 的有效性及资源更新的日期时间等。

使用 HEAD 方法的请求·响应的例子
![](images/HTTP-4.png)

### DELETE 删除文件
DELETE 方法用来删除文件，是与 PUT 相反的方法。DELETE 方法按 请求 URI 删除指定的资源。

但是，HTTP/1.1 的 DELETE 方法本身和 PUT 方法一样不带验证机 制，所以一般的 Web 网站也不使用 DELETE 方法。当配合 Web 应用 程序的验证机制，或遵守 REST 标准时还是有可能会开放使用的。

使用 DELETE 方法的请求·响应的例子
![](images/HTTP-5.png)

### OPTIONS 询问请求的方法
OPTIONS 方法用来查询针对请求 URI 指定的资源支持的方法。

使用 OPTIONS 方法的请求·响应的例子
![](images/HTTP-6.png)