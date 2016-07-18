# 刑技平台客户端 V2.0

[TOC]



## 环境搭建

### 开发工具

* `node `  版本 v4.4.5
* `git`  版本v1.9.2
* `webstorm` 版本 2016.1
* `nw.js`  版本v0.12.0

以上工具FTP上都已上传， 请自行下载安装。

### 代码仓库 

```http
http://192.168.1.103/root/hclient-v2.git
```

将代码克隆并导入到webStorm中，具体略。

### 安装依赖

在工程根目录下，使用下面命令安装依赖，需要联网！

```shell
npm install
```

完成后，所有依赖模块位于`node_modules`文件夹下

### 运行程序

建立快捷运行入口，具体略。参考v1.0文档

## 打包发布

### 打包工具

* `gulp`  和相关插件已安装在node_modules下
* `InnoSetup`  版本 v5

### windows安装包

运行`gulp`任务，运行前需要修改几点

1. 修改setup下的setup.js 文件中的`InnoSetupPath`参数和`InnoSetupConfig`参数。

* `InnoSetupPath` 是InnoSetup根目录下ISCC.exe的绝对路径
* `InnoSetupConfig` 是setup文件夹下的setup.iss的绝对路径

1. 修改setup.iss 文件中`ExeOutputDir`参数和`AppDistDir`参数

* `ExeOutputDir` 是exe文件生成目录
* `AppDistDir` 是工程根目录下的dist文件夹的绝对路径

然后在根目录下运行下面命令，编译生成exe文件

```shell
gulp
```

### 版本更新包





