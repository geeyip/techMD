## 简易部署步骤

### 1. 启动zookeeper服务
将`zookeeper.zip` 解压到任意目录，点击`zookeeper-3.4.6\bin\zkServer.cmd`启动,默认端口`2181`

### 2. 启动基础服务

将`neab.zip`解压到任意目录， 使用`nssm.exe` 安装为系统服务，默认端口`3000`

* 默认端口在server.js中修改（16行）

* 更新程序时，先停止服务，直接解压缩覆盖文件即可，然后重新启动服务

### 3. 启动dubbo服务

将`imms-service-1.0-SNAPSHOT-release.zip` 解压到任意目录，点击`start.bat`启动

* jdbc配置在lib下的 imms-service-1.0-SNAPSHOT.jar 中修改文件jdbc.properties

* zookeeper服务地址在lib下的 imms-service-1.0-SNAPSHOT.jar 中文件dubbo.properties中配置

### 4 . 启动redis服务

使用命令行启动

> redis-server.exe redis.windows.conf

默认端口6379

### 5. 启动tomcat

将 `imms-web.war`  部署到tomcat下

* zookeeper服务地址在 imms-web.war\WEB-INF\classes 下的文件dubbo.properties中配置
* 基础服务地址在 imms-web.war\WEB-INF\classes 下的文件app.properties中配置
* redis服务地址在 imms-web.war\WEB-INF\classes 下的文件redis.properties中配置
