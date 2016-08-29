##不合格现场检查API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/list
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "xczt": "", //现场状态  全部：“0”，合格：“1”，不合格：“2”
  "bhglx": "", //不合格类型  全部：“all”，现场图：“xct”
  "kysjStart": "",  //勘验时间开始
  "kysjEnd": "",  //勘验时间结束
  "faqh": “”, //发案区划
  "kybh": "", //勘验编号
  "ajbh": "", //案件编号
  "jqbh": "",  //警情编号
  "kyr": "", //勘验人
  "kydd": "",  //勘验地点
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
			"kybh": "J110145656985321322",//勘验编号
			"ajbh": "A110145656985321323",//案件编号
			"ajlb": "",//案件类别
			"kysj": "2016-08-19",//勘验时间 Date类型
			"kydd": "朝阳XXX小区",//勘验地点
			"kyr": "某某",//勘验人
			"jcxx": "不合格",//基础信息
			"kybl": "不合格",//勘验笔录
			"xct": "3(不合格)",//现场图
			"xczp":"",//现场照片
			"fxyj": "不合格",//分析意见
			"tqwp": "不合格",//提取物品
			"hj": "",//痕迹
			"dxsl": 1, //短信条数
			"xxsl":2//消息条数
		}
    ],
    "pages": null,
    "operates": null
}
```

​
### 基础信息不合格弹窗展示接口

点击列表中基础信息列中的不合格链接时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/inspect
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/inspect`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "DC3BE807E29C43DFAE58B12A4EA93D3A", //
  "type": "jcxx" //类型：基础信息
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
			"reasons": [
				{"bhgyy": "案件类别未填写"},
				{"bhgyy": "保护人单位未填写"}
			],//不合格原因
			"rdr": "system",//认定人
			"rdsj": "2016-08-23"//认定时间
		}
    ],
    "pages": null,
    "operates": null
}
```

​

### 现场图不合格弹窗展示接口

点击列表中现场图列中的不合格链接时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/inspect
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/inspect`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "DC3BE807E29C43DFAE58B12A4EA93D3A", //
  "type": "xct" //类型：现场图
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
			"reasons": [
				{"bhgyy": "案件类别未填写"},
				{"bhgyy": "保护人单位未填写"}
			],//不合格原因
			"kybh": "K23439484849439",//勘验编号
			"xcfwt": [
				{"name": "方位图1","base64": "/9j/4AAQSkZJRgABAQ......"},
				{"name": "方位图2","base64": "/9j/4AAQSkZJRgABAQ......"}
			],//现场方位图
			"xczxxct": [
				{"name": "中心现场图1","base64": "/9j/4AAQSkZJRgABAQ......"},
				{"name": "中心现场图2","base64": "/9j/4AAQSkZJRgABAQ......"}
			],//现场中心现场图
			"rdr": "system",//认定人
			"rdsj": "2016-08-23",//认定时间
			"rdyj": "各种意见blabla你懂的"//认定意见
		}
    ],
    "pages": null,
    "operates": null
}
```
​

### 现场照片不合格弹窗展示接口

点击列表中现场照片列中的不合格链接时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/inspect
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/inspect`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "DC3BE807E29C43DFAE58B12A4EA93D3A", //
  "type": "xczp" //类型：现场照片
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
			"reasons": [
				{"bhgyy": "案件类别未填写"},
				{"bhgyy": "保护人单位未填写"}
			],//不合格原因
			"kybh": "K23439484849439",//勘验编号
			"xczpfw": [
				{"name": "方位图1","base64": "/9j/4AAQSkZJRgABAQ......"},
				{"name": "方位图2","base64": "/9j/4AAQSkZJRgABAQ......"}
			],//现场照片方位
			"xczpgm": [
				{"name": "概貌1","base64": "/9j/4AAQSkZJRgABAQ......"},
				{"name": "概貌2","base64": "/9j/4AAQSkZJRgABAQ......"}
			],//现场照片概貌
			"xczpzdbw": [
				{"name": "重点部位1","base64": "/9j/4AAQSkZJRgABAQ......"},
				{"name": "重点部位2","base64": "/9j/4AAQSkZJRgABAQ......"}
			],//现场照片重点部位
			"rdr": "system",//认定人
			"rdsj": "2016-08-23",//认定时间
			"rdyj": "各种意见blabla你懂的"//认定意见
		}
    ],
    "pages": null,
    "operates": null
}
```
​
###分析意见不合格弹窗展示接口

点击列表中分析意见列中的不合格链接时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/inspect
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/inspect`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "DC3BE807E29C43DFAE58B12A4EA93D3A", //
  "type": "fxyj" //类型：分析意见
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
			"reasons": [
				{"bhgyy": "案件类别未填写"},
				{"bhgyy": "保护人单位未填写"}
			],//不合格原因
			"rdr": "system",//认定人
			"rdsj": "2016-08-23"//认定时间
		}
    ],
    "pages": null,
    "operates": null
}
```

​
###提取物品不合格弹窗展示接口

点击列表中提取物品列中的不合格链接时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/inspect
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/inspect`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "DC3BE807E29C43DFAE58B12A4EA93D3A", //
  "type": "tqwp" //类型：提取物品
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
			"reasons": [
				{"bhgyy": "案件类别未填写"},
				{"bhgyy": "保护人单位未填写"}
			],//不合格原因
			"kybh": "K489302378239",//勘验编号
			"rdr": "system",//认定人
			"rdsj": "2016-08-23",//认定时间
			"rdyj": ""//认定意见
		}
    ],
    "pages": null,
    "operates": null
}
```

​
###痕迹信息不合格弹窗展示接口

点击列表中痕迹列中的不合格链接时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/bhgxcjc/inspect
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/inspect`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "DC3BE807E29C43DFAE58B12A4EA93D3A", //
  "type": "hj" //类型：痕迹
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
			"reasons": [
				{"bhgyy": "案件类别未填写"},
				{"bhgyy": "保护人单位未填写"}
			],//不合格原因
			"kybh": "K489302378239",//勘验编号
			"rdr": "system",//认定人
			"rdsj": "2016-08-23",//认定时间
			"rdyj": ""//认定意见
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
http://localhost:8080/api/1/qualityCheck/bhgxcjc/_urge
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/_urge`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
http://localhost:8090/api/1/qualityCheck/bhgxcjc/urge
```

后端格式为`/api/{recordLog}/qualityCheck/bhgxcjc/urge`,其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**
```json
{
    "xxnr": "现场勘验号:K1101126644646313232 不合格",  //消息内容
	"sffsdx": 1,  //是否发送短信  1:发送 0:不发送
	"dxnr": "现场勘验号:K1101126644646313232 不合格",  //短信内容
	"fsmdId": "DC3BE807E29C43DFAE58B12A4EA93D3A,DC3BE807E29C43DFAE58B12A4EA93D5H",  //发送名单人员ID以逗号隔开
	"fsmdName": "张三,李四",  //发送名单人员姓名以逗号隔开
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```