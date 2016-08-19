##现场及时关联监督API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/1/workSupervise/xcjsgljd/list
```

后端格式为`/api/{recordLog}/workSupervise/xcjsgljd/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "sfgl": "", //是否关联  未关联：1，已关联：2
  "zdjkajl": "", //重点监控案件类 全部：“zkjkajl_all”，十类必勘验案件：“zkjkajl_slbky”
  "ajlb": "", //案件类别
  "faqh": "",  //发案区划
  "kysjStart": "",  //勘验时间开始
  "kysjEnd": "",  //勘验时间结束
  "kybh": "", //勘验编号
  "ajbh": "", //案件编号
  "jqbh": "", //警情编号
  "kyr": "", //勘验人
  "kydd": "", //勘验地点
  "sfzg": "", //是否整改 全部：0，未整改：1，已整改：2
  "sfyq": "", //是否逾期  全部：0，未逾期：1，已逾期：2
  "xczt": "", //现场状态  全部：""，已提交："ytj"，暂存："zc"等
  "begin": 1,
  "end": 60
}
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data": [
		{
			"rownum": "1",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"xckyh": "J110145656985321322",
			"jqbh": "J110145656985321322",
			"ajbh": "A110145656985321323",
			"kysj": "2016-08-18",//Date类型
			"kydd": "朝阳XXX小区",
			"ajlb": "",
			"faqh": "",
			"fadd": "朝阳XXX小区",
			"kyr": "某某",
			"xczt":"",
			"sfyq": "2",//1:未逾期  2:已逾期
			"dxsl": 1, //短信条数
			"xxsl":2//消息条数
		}
    ],
    "pages": null,
    "operates": null
}
```

​

### 消息发送弹窗展示接口

点击催办按钮时触发

#### API路径

```http
http://localhost:8080/api/1/workSupervise/xcjsgljd/_urge
```

后端格式为`/api/{recordLog}/workSupervise/xcjsgljd/_urge`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数

```
无
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data": [
		{
			"trueName": "周丽",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"postZw": "技术员",
			"mobilephoneNo": "13659856321"
		}
    ],
    "pages": null,
    "operates": null
}
```


### 消息发送页信息保存接口

点击催办弹窗的保存按钮触发

#### API 路径

```http
http://localhost:8090/api/1/workSupervise/xcjsgljd/urge
```

后端格式为`/api/{recordLog}/workSupervise/xcjsgljd/urge`,其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**
```json
{
    "xxnr": "现场勘验号:K1101126644646313232 逾期未关联",  //消息内容
	"sffsdx": 1,  //是否发送短信  1:发送 0:不发送
	"dxnr": "现场勘验号:K1101126644646313232 逾期未关联",  //短信内容
	"fsmdId": "DC3BE807E29C43DFAE58B12A4EA93D3A,DC3BE807E29C43DFAE58B12A4EA93D5H",  //发送名单人员ID以逗号隔开
	"fsmdName": "张三,李四",  //发送名单人员姓名以逗号隔开
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```