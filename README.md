## 1. 创建服务器
## 2. 监听客户端的请求
## 3. 从连接中读取数据
## 4. 保存所有的客户端
## 5. 广播数据
## 6. 删除被关闭的连接

## 参数
用putty连接时会回传一串奇怪的内容。
```
​FF FB 1F FF FB 20 FF FB 18 FF FB 27 FF FD 01 FF FB 03 FF FD 03
```
这是因为telnet连接并不是单纯的TCP,会僻壤 一参数过去设计telnet的属性


- FF FB 1F window size
- FF FB 20 terminal speed
- FF FB 18 terminal type
- FF FB 27 Telnet Environment Option
- FF FD 01 echo
- FF FB 03 suppress go ahead
- FF FD 03 suppress go ahead

如果不需要可以使用`RAW`模式即可