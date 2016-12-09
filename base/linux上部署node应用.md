## lINUX上部署NODE应用

### 软件清单

* `node-v4.4.4-linux-x64.tar.gz`
* `query-web.tar.gz`



### 安装步骤

#### 安装nodejs

解压缩node安装包

```shell
tar -xv -f node-v4.4.4-linux-x64.tar.gz -C /opt
```

建立连接，使能全局使用node命令

```shell
ln -s /opt/node-v4.4.4-linux-x64/bin/node /usr/local/bin/node
```

安装验证

```shell
node -v
```



#### 部署web应用

解压缩程序包

```shell
tar -xv -f query-web.tar.gz -C /opt
```

进入程序文件夹

```shell
cd /opt/query-web
```

启动程序

```shell
nohup node server > myLog.log 2>&1 &
```

部署验证

浏览器访问`http://localhost:3000`



