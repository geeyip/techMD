##  基础服务主要API

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