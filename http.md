#### http和https协议有什么区别，重点解释https

#### http
1. http+加密+认证#### http和https协议有什么区别，重点解释https

1. http+加密+认证+完整性保护=https
2. http:应用层的无状态，超文本传输协议。端口为80

3. HTTPS：只是http通信接口部分用SSL和TLS协议替代。http直接和TCP通信，而HTTPS使用SSL所以是先和SSL通信，再由SSL和TCP通信。端口为443

#### cookie sessionStorage localStorage有什么不同

- cookie存储在客户端，可以发送给服务器，数据大小限制为4K

- sessionStorage,localStorage存储在本地，不可以发送给服务器，数据大小为5M

- localStorage只能手动清除数据

- sessionStorage关闭会话窗，数据就被清除了

#### DNS解析域名为IP

- 浏览器缓存中找

- 系统缓存中找

- 路由器缓存中找

- ISP DNS缓存中找

#### TCP三次握手

- client----->server:SYN(发起一个TCP连接，同步报文)

- server----->client:SYN+ACK(应答报文，表示已创建连接)

- client----->server:ACK(应答报文，表示收到已连接)

##### 四次挥手：
    由客户端发起的关闭连接
        * client----->server:FIN(请求关闭连接)
        * server----->client:ACK(收到了连接，但不会立即关闭，等到报文都发送完再回复一个FIN)
        * server----->client:FIN
        * client----->server:ACK(收到关闭)

    由服务端发起的关闭连接
        * 当http设置了keepalive定时关闭，服务端会在结束数据传送后关闭TCP连接

#### http请求

- 请求行

- 请求头

- 空行

- 请求包体(只有POST请求有包体)

#### get/post区别

1. 请求参数：get参数附在URL后面?隔开，POST参数放在包体中

2. 大小限制：GET限制为2048字符，post无限制

3. 安全问题：GET参数暴露在URL中，不如POST安全

4. 浏览器历史记录：GET可以记录，POST无记录

5. 缓存：GET可被缓存，post无

6. 书签：GET可被收藏为书签，post不可

7. 数据类型：GET只能ASCII码，post无限制

#### onload ready区别：

ready表示文档加载完毕，不包括图片

onload表示都加载完毕

#### http响应

- 状态行

- 响应头

- 响应包体

##### http状态码

- 1XX：表示可续发请求

- 2XX：表示成功

 * 202成功
 * 204成功 不返回实体主体
 * 206成功 执行了一个范围请求
- 3XX：表示重定向
 * 301永久重定向，增加SEO排名
 * 302临时重定向 禁止POST变为GET
 * 303另外一个URI
 * 304判断是否要更新缓存 请求头部携带if-modified-since自从上次更新距这次多久
 * 307临时重定向
- 4XX：表示客户端错误
 * 400客户端语法错误
 * 401请求未经授权
 * 403服务器拒绝服务
 * 404请求资源不存在
- 5XX：服务端错误
 * 500不可预期的错误
 * 503此时不能提供服务 稍后恢复正常
#### 释放TCP连接
header中的connecton:close

服务器主动关闭TCP连接，客户端被动关闭连接
header中的connecton:keepalive

连接保持一段时间，可以连续发送http请求+完整性保护=https
2. http:应用层的无状态，超文本传输协议。端口为80

3. HTTPS：只是http通信接口部分用SSL和TLS协议替代。http直接和TCP通信，而HTTPS使用SSL所以是先和SSL通信，再由SSL和TCP通信。端口为443

#### cookie sessionStorage localStorage有什么不同

- cookie存储在客户端，可以发送给服务器，数据大小限制为4K

- sessionStorage,localStorage存储在本地，不可以发送给服务器，数据大小为5M

- localStorage只能手动清除数据

- sessionStorage关闭会话窗，数据就被清除了

#### DNS解析域名为IP

- 浏览器缓存中找

- 系统缓存中找

- 路由器缓存中找

- ISP DNS缓存中找

#### TCP三次握手

- client----->server:SYN(发起一个TCP连接，同步报文)

- server----->client:SYN+ACK(应答报文，表示已创建连接)

- client----->server:ACK(应答报文，表示收到已连接)

##### 四次挥手：
    由客户端发起的关闭连接
        * client----->server:FIN(请求关闭连接)
        * server----->client:ACK(收到了连接，但不会立即关闭，等到报文都发送完再回复一个FIN)
        * server----->client:FIN
        * client----->server:ACK(收到关闭)

    由服务端发起的关闭连接
        * 当http设置了keepalive定时关闭，服务端会在结束数据传送后关闭TCP连接

#### http请求

- 请求行

- 请求头

- 空行

- 请求包体(只有POST请求有包体)

#### get/post区别

1. 请求参数：get参数附在URL后面?隔开，POST参数放在包体中

2. 大小限制：GET限制为2048字符，post无限制

3. 安全问题：GET参数暴露在URL中，不如POST安全

4. 浏览器历史记录：GET可以记录，POST无记录

5. 缓存：GET可被缓存，post无

6. 书签：GET可被收藏为书签，post不可

7. 数据类型：GET只能ASCII码，post无限制

#### onload ready区别：

ready表示文档加载完毕，不包括图片

onload表示都加载完毕

#### http响应

- 状态行

- 响应头

- 响应包体

##### http状态码

- 1XX：表示可续发请求

- 2XX：表示成功

 * 202成功
 * 204成功 不返回实体主体
 * 206成功 执行了一个范围请求
- 3XX：表示重定向
 * 301永久重定向，增加SEO排名
 * 302临时重定向 禁止POST变为GET
 * 303另外一个URI
 * 304判断是否要更新缓存 请求头部携带if-modified-since自从上次更新距这次多久
 * 307临时重定向
- 4XX：表示客户端错误
 * 400客户端语法错误
 * 401请求未经授权
 * 403服务器拒绝服务
 * 404请求资源不存在
- 5XX：服务端错误
 * 500不可预期的错误
 * 503此时不能提供服务 稍后恢复正常
#### 释放TCP连接
header中的connecton:close

服务器主动关闭TCP连接，客户端被动关闭连接
header中的connecton:keepalive

连接保持一段时间，可以连续发送http请求