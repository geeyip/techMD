# neab.zip部署说明

## 依赖

*  neab是基于`node`开发的，所以部署前需要安装node，版本>= 4.4.5。

* neab使用`mongodb`存储数据，所以也需要安装。

## 部署

部署方式，使用`nssm.exe`注册为windows系统服务。步骤如下：
* 将neab.zip解压到neab文件夹(其他名称也可)。


* 在neab文件夹下打开命令窗口（最好是以管理员权限打开命令窗口），输入命令`nssm install` 打开服务安装界面。


* 各参数填写 如下 

​	`Path`： 选择node安装目录下的`node.exe `

​	`	Startup directory` ： 选择neab文件夹所在路径。

​	`	Arguments` ：填写server。

​	`Service name` ：neab ,或自己定义。

* 填好后点击Install service 即可，最后启动服务。


* 通过地址http://localhost:3000 验证服务是否正常启动。

## 配置

* 服务启动失败，可能端口被占用，默认端口（3000）在server.js中修改（16行）。


* mongodb的连接地址配置在resource/setting.json中配置。


* imms-web.war中，需要修改app.properites文件中socket.server.url 和 upload.server.url 的地址改成neab服务的地址。
