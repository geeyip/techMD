##  基础服务主要API

### 连接socket

引入`socket.io.js`

```javascript
var socket = null;
var userInfo = {
  userId:  'sys',
  userName: '管理员',
  userUnit: '厦门市公安局',
  systemId: 'YTHPT',
  systemPlace: '350200000000'
};
//连接Socket
socket = io.connect('http://192.168.1.155:3000');
//登录事件
socket.emit('login', userInfo);
//监听登出
socket.on('logoutAll', function(){
  logout();
});
```



### 获取在线用户

获取在线用户集合与在线用户数

```http
GET http://ip:port/api/online/users?systemId={systemId}&systemPlace={systemPlace}
```

```http
GET http://ip:port/api/online/users/count?systemId={systemId}&systemPlace={systemPlace}
```

- `systemId`  系统ID，必须传递
- `systemPlace` 系统12位部署地代码

API返回JSON数组示例

```json
[
  {
  	"userId":"test(用户名)",
  	"userName":"李四(用户姓名)",
  	"userUnit":"350200000000(用户12位单位代码)",
  	"systemId":"YTHPT",
 	"systemPlace":"330100000000",
    "ip":"192.168.1.11(用户IP地址)",
  	"loginTime":"2016-12-05 17:32:09(用户登录时间)"
	}
]
```



### 获取登录登出日志

```http
POST http://ip:port/api/online/logs?systemId={systemId}&systemPlace={systemPlace}
```

- `systemId`  系统ID，必须传递
- `systemPlace` 系统12位部署地代码

分页查询传递`jsonStr`参数示例

```json
{
  "oprUser":"sys",
  "logDateBegin":"2016-12-05",
  "logDateEnd":"2016-12-05",
  "begin":1,
  "end":200,
  "sortName":"LOG_TIME",
  "sortOrder": "desc"
}
```

* `oprUser` 登录用户名
* `logDateBegin`和`logDateEnd` 登录时间开始、登录时间结束
* `begin` 和 `end` 返回分页数据开始与结束序号
* `sortName `、`sortOrder` 排序字段与排序方式,，`sortName `有`LOG_TIME`与`OFF_TIME`可选，`sortOrder`有`desc`与`asc`可选

API返回JSON对象示例

```json
{
  "flag":1,  
  "totalCount":1,
  "data":[
    {
      "oprUser":"sys(用户名)",
      "oprUserName":"张三(用户姓名)",
      "oprUnit":"350200000000(用户12位单位代码)",
      "logTime":"2016-12-05 17:09:23(登录时间)",
      "offTime":"2016-12-05 17:26:01(登出时间)",
      "ip":"192.168.1.11(用户IP地址)",
      "rn":1
    }
  ]
}
```

* `flag` 查询标记，1-成果 0-异常
* `totalCount`查询数据总条数
* `data`分页数据，其中`rn`为数据序号



### 文件上传服务

**文件上传**

```http
POST http://ip:port/api/file/upload
```

上传表单示例

```html
<form method="post" action="http://ip:port/api/file/upload" enctype='multipart/form-data'>
    <fieldset>
        <div class="form-group">
            <label class="col-sm-2 control-label">选择文件</label>
            <div class="col-sm-5">
                <input id="test" name="test" type="file" class="form-control" />
            </div>
        </div>
        <div class="form-group">
            <div class="col-sm-4">
                <button id="btnSub" class="btn btn-sm btn-primary" type="submit">上 传</button>
            </div>
        </div>
    </fieldset>
</form>
```

* `enctype='multipart/form-data'` 表单的`enctype`需要指定为`multipart/form-data`
* 目前只支持单文件的上传，多文件上传开发中

异步上传示例

```javascript
var formData = new FormData();
formData.append("myfile", document.getElementById("test").files[0]);   
$.ajax({
    url: "http://localhost:3000/api/file/upload",
    type: "POST",
    data: formData,
    contentType: false,
    processData: false,
    success: function (data) {
      if(data.flag == '1'){
        alert('上传成功');
        console.log(data.fileId);
      }
    },
    error: function () {
      alert("上传失败！");
    }
});
```

上传成功返回示例

```json
{
  "flag":1,
  "msg":"上传成功",
  "fileId":"5846908f0d0b16013dcc3c3b"
}
```

* `fileId` 服务端生成的文件唯一ID，下载与删除文件需要传递此ID

  ​

**文件下载**

```http
GET http://ip:port/api/file/download/{id}
```

* `id`  文件ID
* 需要浏览器中直接预览文件，比如图片、文本，需要传递参数`preview`，可在API后加 `?preview=true`

**文件删除**

```http
GET http://ip:port/api/file/delete/{id}
```

* `id`  文件ID

### 客户端个更新相关

客户端检查更新
```http
GET http://ip:port/api/client/version?systemId={systemId}&systemPlace={systemPlace}&version={version}
```

* `systemId`  系统ID，必须传递
* `systemPlace` 系统12位部署地代码，必须传递
* `version` 客户端本地版本序列号

返回示例

```json
{
  "latestVersion":1481103947524,
  "localVersion":"-1",
  "update":true,
  "fileId":"5847da4ac1a2d82a8ca537b4",
  "desc":"1. 界面优化\r\n2. 其他优化"
}
```

* `latestVersion`最新版本序列号
* `localVersion`本地版本序列号
* `update` 是否需要更新
* `fileId`更新包文件ID
* `desc` 更新内容说明

客户端安装包下载
```http
GET http://ip:port/api/client/install?systemId={systemId}&systemPlace={systemPlace}
```
* `systemId`  系统ID，必须传递
* `systemPlace` 系统12位部署地代码，必须传递