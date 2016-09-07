## 一体化客户端打包

### 安装环境

打包开始前，需要安装下列软件

* Node [点击下载](https://nodejs.org/en/download/)
* Inno Setup  [点击下载](https://pan.baidu.com/s/1c18kJ0O)

### 克隆代码

```shell
git clone https://github.com/geeyip/one-client.git
```

使用`webstorm` 从代码仓库克隆代码，克隆后的文件结构如下

![](pic/p1.png)

其中**data**与**dist** 文件夹为一体化前端代码,需要从一体化工程中拷贝到这里， **node_modules** 文件夹刚开始不存在，需要安装依赖生成。

### 拷贝一体化代码

将一体化工程webapp下的data文件夹、dist文件夹、package.json文件拷贝到工程目录下覆盖。

### 安装依赖

```shell
npm install
```

在`webstorm`的命令窗口(`Terminal`) , 使用上面命令安装依赖, 完成后生成**node_modules** 文件夹。

### 修改配置

根据`Inno Setup`安装路径的不同和`one`工程克隆存放路径的不同，需要修改配置文件。

**修改`setup`文件夹下的`setup.js` 文件，修改下列2处**

```javascript
exports.InnoSetupPath = "D:\\InnoSetup5\\ISCC.exe";

exports.InnoSetupConfig = "E:\\work\\one\\setup\\setup.iss";
```

`InnoSetupPath` 是`Inno Setup`安装根目录下`ISCC.exe`的绝对路径

`InnoSetupConfig` 是`setup`文件夹下的`setup.iss`文件的绝对路径

**修改`setup`文件夹下的`setup.iss` 文件，修改下列2处**

注意，`webstorm`打开会有乱码，所以使用`Inno Setup`软件打开。

```shell
#define ExeOutputDir "D:\"
#define AppDistDir "E:\work\one\tmp"
```

`ExeOutputDir` 是exe安装文件生成存放目录

`AppDistDir` 是`one`工程根目录下的`tmp`文件夹的绝对路径

### 生成安装包

```shell
gulp
```

在`webstorm`的命令窗口(`Terminal`) , 使用上面命令生成安装包, 完成后会在`{ExeOutputDir}` 目录生成windows安装包。






