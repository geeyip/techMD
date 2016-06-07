## 系统登录日志实现

### 应用背景

查看老框架的用户登录日志，会发现很多日志的登出时间为空，这是由于客户端浏览器关闭后没有再去更新登出时间引起的。为了应对新框架的新模式并且解决老框架遗留的问题，决定使用新技术websocket实现用户登录日志的记录。

### 主要技术

* Node

* Express

* socket.io

  ```http
  http://192.168.1.103/root/h-socket.git
  ```

  使用webstorm检出代码，根目录下startup.js 文件使用右键直接运行。运行后直接访问`http://localhos:30000`  

### 实现原理

* 新框架的主页面为index.jsp ，在这个页面进入后会尝试建立socket连接。

  ```javascript
  socket = io.connect('http://localhost:3000');
  ```

* 连接socket服务器h-socket成功后，页面向服务器发送登录事件

  ```javascript
  socket.emit('login', userInfo);
  ```

* 服务器h-socket 端触发登录事件

  ```javascript
  socket.on('login',function(userInfo){
    
  });
  ```

  在服务端h-socket会维护socket连接信息集合与登录用户信息集合，每次进入就将socket连接加入连接集合，如果用户集合中没有当前用户，将当前用户信息加入用户集合，并且记录登入日志。

* 服务器h-socket 端触发断开事件

  浏览器刷新、关闭、index.jsp页面跳转都将触发断开事件

  ```javascript
  socket.on('disconnect', function(){
    
  });
  ```
  连接断开，从连接集合中移除当前连接，延迟3秒判断（主要应对刷新）连接对应的用户是否还保持其他的连接，如果没有就从用户集合中移除当前用户，并且记录登出日志。

* 注销

  浏览器发送注销事件

  ```javascript
  socket.emit('logout',userInfo.userId);
  ```

  服务端触发注销事件

  ```javascript
  socket.on('logout',function(userId){
    
  });
  ```

  ​服务端通过查找所有当前用户保持的连接，并向所有保持的连接发送登出事件。

  ```javascript
   var allSocket = socketStore.findSocketByUserIdAndIp(userId, ip);
   //通知所有连接断开
   allSocket.forEach(function(so){
      so.emit('logoutAll');
   });
  ```

