# Angular测试环境搭建 #

2015-1-16 by *yejiansuo*

![](http://i.imgur.com/tBRBb83.png)
  
**这个文档只介绍测试环境怎么搭建**。

## 开发工具 ##

前端Angular测试需要**Node**支持，如没有安装，请下载对应版本并安装  

- 64位系统
[node-v0.10.28-x64](ftp://hi:hi@192.168.1.168/%BF%AA%B7%A2%B9%A4%BE%DF/node-v0.10.28-x64.msi)

- 32位系统
[node-v0.10.28-x86](ftp://hi:hi@192.168.1.168/%BF%AA%B7%A2%B9%A4%BE%DF/node-v0.10.28-x86.msi)

前端开发及测试使用的IDE为**WebStorm**,如没有安装请下载安装 [WebStorm 9.0](ftp://hi:hi@192.168.1.168/%BF%AA%B7%A2%B9%A4%BE%DF/WebStorm-9.0.exe)

安装完成后，将前端工程(webapp)导入WebStorm。

## 单元测试 ##

前端单元测试使用的框架为**Karma**和**Jasmine**。为了能正常运行单元测试前，需要先安装Karma、Jasmine和其他测试相关的Node模块。
Node模块的安装使用包管理器NPM,安装的方式有2种。全局安装和当前目录安装。建议使用全局安装，以后新check out的工程就不需要重新搭建测试环境了。


### 全局安装 ###

在命令串口输入命令 `npm install -g karma` **注意 -g 代表全局安装，不能省略**

> C:\Users\Administrator>npm install -g karma 

等待自动安装完成，出现如下时表示安装成功！

	karma@0.12.31 C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma
	├── graceful-fs@2.0.3
	├── di@0.0.1
	├── colors@0.6.2
	├── rimraf@2.2.8
	├── mime@1.2.11
	├── q@0.9.7
	├── lodash@2.4.1
	├── minimatch@0.2.14 (sigmund@1.0.0, lru-cache@2.5.0)
	├── useragent@2.0.10 (lru-cache@2.2.4)
	├── source-map@0.1.43 (amdefine@0.1.0)
	├── optimist@0.6.1 (wordwrap@0.0.2, minimist@0.0.10)
	├── glob@3.2.11 (inherits@2.0.1, minimatch@0.3.0)
	├── log4js@0.6.22 (semver@1.1.4, async@0.2.10, readable-stream@1.0.33)
	├── http-proxy@0.10.4 (pkginfo@0.3.0, utile@0.2.1)
	├── chokidar@0.12.6 (async-each@0.1.6, readdirp@1.3.0)
	├── socket.io@0.9.16 (base64id@0.1.0, policyfile@0.0.4, redis@0.7.3, socket.io-client@0.9.16)
	└── connect@2.26.6 (cookie@0.1.2, media-typer@0.3.0, cookie-signature@1.0.5...

**C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma** 即karma的安装路径，后面要用到。

这时在命令行输入

>C:\Users\Administrator>karma

会提示 'karma' 不是内部或外部命令，也不是可运行的程序或批处理文件。要在命令行使用karma指令，还需要安装**karma-cli**

> C:\Users\Administrator>npm install -g karma-cli 

	C:\Users\Administrator\AppData\Roaming\npm\karma -> C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-cli\bin\karma
	karma-cli@0.0.4 C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-cli
	└── resolve@0.5.1

再在命令行输入karma指令

	C:\Users\Administrator>karma
	Command not specified.
	Karma - Spectacular Test Runner for JavaScript.
	
	Usage:
	  node C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-cli\bin\kar
	ma <command>
	
	Commands:
	  start [<configFile>] [<options>] Start the server / do single run.
	  init [<configFile>] Initialize a config file.
	  run [<options>] [ -- <clientArgs>] Trigger a test run.
	  completion Shell completion for karma.
	
	Run --help with particular command to see its description and available options.
	
	
	Options:
	  --help     Print usage and options.
	  --version  Print current version.

完成！ 接着安装Jasmine,安装基本同karma

> C:\Users\Administrator>npm install -g jasmine

	C:\Users\Administrator>npm install -g jasmine
	C:\Users\Administrator\AppData\Roaming\npm\jasmine -> C:\Users\Administrator\AppData\Roaming\npm\node_modules\jasmine\bin\jasmine.js
	jasmine@2.1.1 C:\Users\Administrator\AppData\Roaming\npm\node_modules\jasmine
	├── jasmine-core@2.1.3
	└── glob@3.2.11 (inherits@2.0.1, minimatch@0.3.0)

最后，需要安装以下几个插件，不解释，一看名字就知道大概是什么用的！

- karma-jasmine 
- karma-chrome-launcher
- karma-ie-launcher
- karma-coverage
- karma-junit-reporter

安装多个Node模块，使用空格分隔即可

> E:\>npm install -g karma-jasmine karma-ie-launcher karma-chrome-launcher karma-coverage karma-junit-reporter

	karma-chrome-launcher@0.1.7 C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-chrome-launcher
	karma-ie-launcher@0.1.5 C:\Users\Administrator\AppData\Roaming\npm\node_modules\
	karma-ie-launcher
	karma-junit-reporter@0.2.2 C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-junit-reporter
	└── xmlbuilder@0.4.2
	jasmine-core@2.1.3 C:\Users\Administrator\AppData\Roaming\npm\node_modules\jasmine-core
	karma-jasmine@0.3.4 C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-jasmine
	karma-coverage@0.2.7 C:\Users\Administrator\AppData\Roaming\npm\node_modules\karma-coverage
	├── minimatch@0.3.0 (sigmund@1.0.0, lru-cache@2.5.0)
	├── ibrik@2.0.0 (which@1.0.8, estraverse@1.8.0, lodash@2.4.1, esprima@1.2.2,
	coffee-script@1.8.0, mkdirp@0.5.0, optimist@0.6.1, fileset@0.1.5)
	├── dateformat@1.0.11 (get-stdin@3.0.2, meow@2.1.0)
	└── istanbul@0.3.5 (which@1.0.8, abbrev@1.0.5, wordwrap@0.0.2, nopt@3.0.1...

现在，可以使用karma去单元测试了。

### 命令行进行单元测试 ###

定位到前端工程根目录下的test目录，在命令窗口中使用命令 `karma start` 启动Karma服务，再使用 `Karma run` 运行单元测试 。
启动服务时会打开IE或Chrome浏览器，不要关掉 ，因为测试依赖浏览器环境。当然启动服务的命令窗口也不能关，因为窗口关闭，服务就停止了，所以，karma run 需打开另外一个窗口运行。

> E:\repository\mvc-root\modules\mvc-angular\src\main\webapp\test>karma start

	INFO [karma]: Karma v0.12.31 server started at http://localhost:9876/
	INFO [launcher]: Starting browser Chrome
	INFO [Chrome 36.0.1985 (Windows 7)]: Connected on socket OZsB9Ba6dN9nGpru2nzK wi
	th id 48314589

打开另外一个命令窗口。

>E:\repository\mvc-root\modules\mvc-angular\src\main\webapp\test>karma run

开始运行所有单元测试用例，并在命令窗口中打印测试结果。成功输出绿色SUCCESS,失败输出红色FAILED 。

使用命令是不是很烦，不能直接定位失败代码等，不够高效，所以还是和IDE集成吧，怎么和Webstorm集成？往下看...

### 当前目录安装 ###

基本可以直接跳过，如果你不打算使用这种方式。

当前目录安装则只需使用命令`npm install`就可以。在前端工程根目录下，输入如下命令。

> E:\repository\mvc-root\modules\mvc-angular\src\main\webapp>npm install

将会安装package.json中定义的模块。但是当前目录安装无法直接使用命令行进行单元测试，需要集成WebStorm才行。

### Karma与WebStorm 集成 ###
步骤如下：

1. 点击Webstrom的菜单栏**Run** 

2. 选择**Edit Configurations**

3. 点击左上角加号**+** ，并选择**Karma**

4. 左侧填写: `Name` 自己定义(Karma)，`Configuration file` 选择**test**目录下的**karma.conf.js**，下拉选择即可。其他默认即可。
需要注意的是`Karma package` 是根据你安装Karma的方式（全局安装还是当前目录安装）选择的。

5. 点击OK。

配置完成，点击Webstrom的菜单栏**Run** ，下拉选择 Run 'Karma(或你的名称)' ,或使用命令栏的按钮,即可进行单位测试。WebStorm启动服务的同时还运行了的单元测试。一步到位。图形界面展示测试结果，并能快速定位测试失败代码，更能根据修改文件后自动运行单元测试等。更多内容需你自己探索，到这里单位测试的环境搭建就完了！

## 端到端测试 ##

端到端测试，就是让机器模拟用户行为来测试功能的可靠性，是一种黑盒测试。  
我们主要使用Protractor框架来完成端到端测试。这里只介绍全局安装方式。

先全局安装Protractor

> C:\Users\Administrator>npm install -g protractor

安装完成后，需要下载selenium-server 和 chromedriver,你用如下命令

> C:\Users\Administrator>webdriver-manager update

你肯定下载失败，因为这2个文件都在谷歌的服务器上。只能手动下载了.

- [selenium-server-standalone](ftp://hi:hi@192.168.1.168/%BF%AA%B7%A2%B9%A4%BE%DF/selenium-server-standalone-2.40.0.jar)
- [chromedriver](ftp://hi:hi@192.168.1.168/%BF%AA%B7%A2%B9%A4%BE%DF/chromedriver.rar)

下载后，将selenium-server-standalone-2.40.0.jar 放到protractor安装目录下的selenium下，我的目录是

> C:\Users\Administrator\AppData\Roaming\npm\node_modules\protractor\selenium

同样chromedriver.rar解压后的文件chromedriver.exe也拷贝到该目录下(其他也行的)。

最后将C:\Users\Administrator\AppData\Roaming\npm\node_modules\protractor\selenium 目录加入系统Path。就是 chromedriver.exe 所在目录加入Path。

### 命令行运行端到端测试 ###


定位到前端工程根目录下的test目录，在命令窗口中使用命令 `webdriver-manager start` 启动selenium-server，再使用 `protractor` 运行单元测试，

先启动selenium-server

> E:\repository\mvc-root\modules\mvc-angular\src\main\webapp\test>webdriver-manager start、

运行端到端测试

> E:\repository\mvc-root\modules\mvc-angular\src\main\webapp\test>protractor

此时测试框架会自动打开浏览器，自动完成所有操作，并打印测试结果。


### Protractor与WebStorm集成 ###

步骤如下：

1. 点击Webstrom的菜单栏**Run** 

2. 选择**Edit Configurations**

3. 点击左上角加号+ ，并选择**Node.js**

4. 左侧填写: `Name` 自己定义(Protractor)，`JavaScript file` 选择protractor安装目录下的 lib 目录下 的 cli.js 文件,我的填写为  
> C:\Users\Administrator\AppData\Roaming\npm\node_modules\protractor\lib\cli.js  

`Application parameters` 选择工程test目录下的protractro.conf.js文件， 填写为(大家的应该一样)  

> test\protractor.conf.js

其他都默认。

5. 点击OK。

配置完成，点击Webstrom的菜单栏**Run** ，下拉选择 Run 'Protractor（或你的名称）' ,或使用命令栏的按钮,即可进行端到端测试。

***

2015-1-16 by yejiansuo


*** 




