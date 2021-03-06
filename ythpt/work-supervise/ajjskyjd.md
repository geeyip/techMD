##案件及时勘验监督API文档

### 页面查询接口

点击查询按钮时触发

#### API路径 

```http
http://localhost:8080/api/1/workSupervise/ajjskyjd/list
```

后端格式为`/api/{recordLog}/workSupervise/ajjskyjd/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "sfky": "", //是否勘验  全部：0，未勘验：1，已勘验：2
  "zdjkajl": "", //重点监控案件类
  "ajlb": "", //案件类别
  "fadpcs": "",  //发案地所辖派出所
  "lasjStart": "",  //立案时间开始
  "lasjEnd": "",  //立案时间结束
  "jqbh": "", //警情编号
  "ajbh": "", //案件编号
  "jyaq": "", //简要案情
  "sspq": "", //所属片区
  "fadd": "", //发案地点
  "sfzg": "", //是否整改 全部：0，未整改：1，已整改：2
  "sfyq": "", //是否逾期  全部：0，未逾期：1，已逾期：2
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
			"jqbh": "J110145656985321322",
			"ajbh": "A110145656985321323",
			"fadsxpcs": "XXX派出所",
			"ajlb": "入室盗窃",
			"ajzt": "",
			"lasj": "2016-08-18",//Date类型
			"zbdw": "某某单位",
			"zbrxm": "某某",
			"fadd": "朝阳XXX小区",
			"jyaq": "朝阳XXX小区入室盗窃",
			"kyr": "某某",
			"xkbh":"",
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
http://localhost:8080/api/1/workSupervise/ajjskyjd/_urge
```

后端格式为`/api/{recordLog}/workSupervise/ajjskyjd/_urge`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
http://localhost:8090/api/1/workSupervise/ajjskyjd/urge
```

后端格式为`/api/{recordLog}/workSupervise/ajjskyjd/urge`,其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**
```json
{
    "xxnr": "案件编号：A1212456466465465 入室盗窃逾期未勘验",  //消息内容
	"sffsdx": 1,  //是否发送短信  1:发送 0:不发送
	"dxnr": "案件编号：A1212456466465465 入室盗窃逾期未勘验",  //短信内容
	"fsmd": "DC3BE807E29C43DFAE58B12A4EA93D3A,DC3BE807E29C43DFAE58B12A4EA93D5H",  //发送名单，人员ID以逗号隔开
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```