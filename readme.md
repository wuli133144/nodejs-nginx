#说明
这个项目是一个测试项目，旨在配置web开发环境
##特点
*nginx负载均衡高并发
*nodejs处理请求
*异步回调编程

#配置
##nginx:
```
        location / {
              proxy_pass   http://127.0.0.1:8080;
              proxy_redirect default ;
        }
```

##node.js
```
var http = require('http');
http.createServer(function (request, response) {
	// 发送 HTTP 头部 
	// HTTP 状态值: 200 : OK
	// 内容类型: text/plain
	response.writeHead(200, {'Content-Type': 'text/plain'});

	// 发送响应数据 "Hello World"
	response.end('Hello World\n');
}).listen(8080);

// 终端打印如下信息
console.log('Server running at http://127.0.0.1:8888/');
```

#output
Server running at http://127.0.0.1:8888/
