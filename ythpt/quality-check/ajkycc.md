##案件勘验抽查API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/ajkycc/list
```

后端格式为`/api/{recordLog}/qualityCheck/ajkycc/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "lasjStart": "",  //立案时间开始
  "lasjEnd": "",  //立案时间结束
  "ccsl": 10, //抽查数量
  "dw": "", //单位
  "ajlb": "", //案件类别
  "lsccjg": "",  //历史抽查结果
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
			"lasj": "2016-08-18",//立案时间 Date类型
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
### 获取历史抽查结果名称接口

进入页面时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/ajkycc/check_name
```

后端格式为`/api/{recordLog}/qualityCheck/ajkycc/check_name`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
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
			"key": "",
			"value": "20150131 盗抢骗案件抽查"
		},
		{
			"key": "",
			"value": "20150131 入室盗案件抽查"
		}
    ],
    "pages": null,
    "operates": null
}
```

​
### 保存抽查结果接口

点击保存抽查结果按钮时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/ajkycc/check_save
```

后端格式为`/api/{recordLog}/qualityCheck/ajkycc/check_save`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "checkResultName": "",  //抽查结果名称
  "kybhs":["K1101126644646313232", "K1101126644646315698"] //现场勘验号们
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

​

### 消息发送弹窗展示接口

点击催办按钮时触发

#### API路径

```http
http://localhost:8080/api/1/qualityCheck/ajkycc/_urge
```

后端格式为`/api/{recordLog}/qualityCheck/ajkycc/_urge`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
http://localhost:8090/api/1/qualityCheck/ajkycc/urge
```

后端格式为`/api/{recordLog}/qualityCheck/ajkycc/urge`,其中{recordLog}为前端传入，标识是否需要记录操作日志。

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