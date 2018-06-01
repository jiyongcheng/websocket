# websocket
simple websocket example

参考了这篇文章:https://qiutc.me/post/websocket-guide.html

WebSocket 是 HTML5 中提出的新的网络协议标准，其包含几个特点：

建立于 TCP 协议之上的应用层；
一旦建立连接（直到断开或者出错），服务端与客户端握手后则一直保持连接状态，是持久化连接；
服务端可通过实时通道主动下发消息；
数据接收的「实时性（相对）」与「时序性」；

客户端就是在浏览器端的使用,链接ws服务器,如果连接上了,就可以给服务器发送消息,或者接受消息
主要的用法:
const ws = new WebSocket('ws://localhost:8080');
ws.send('send message to server');
ws.onmessage 监听机制,监听从服务器过来的消息,然后处理这个消息
ws.close();关闭链接
ws.onclose 在服务器关闭链接时候的处理
ws.onerror 当出错了做的处理


服务器端也可以处理
send 发送消息
on('connection') 监听链接
on('message')监听消息

使用express,可以参考express的网站安装和启动服务https://expressjs.com/en/starter/installing.html



