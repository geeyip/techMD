## 现场照片现场检查API文档

### 一、页面查询接口

点击查询按钮时触发

#### API路径 

```http
http://localhost:8090/api/1/qualityCheck/xczp/list
```

后端格式为`/api/{recordLog}/qualityCheck/xczp/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "sfsc":"",  //是否审查
  "sfhg":"", //是否合格
  "sfzg":"",//是否整改
  "investigationTimeStart": "",//勘验开始时间
  "investigationTimeEnd": "",//勘验结束时间
  "faqh": "",//发案区划
  "investigationNo": "",//勘验编号
  "caseNo": "", //案件编号
  "jqbh": "",//警情编号
  "investigationPlace": "",//勘验地点
  "investigator": ""//勘验人
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
			"investigationId": "6E806CAB765A4051932A948F97BDC57A", //勘验id
			"investigationNo": "K1101126644646313233",//勘验编号
			"ajbh": "A12312315451321211",//案件编号
			"jqbh": "J110145656985321324",//警情编号
			"caseType": "入室盗窃",//案件类别
			"faqh": "xxx",//发案区划
			"fadd": "xxx",//发案地点
			"investigationTime": "2015-01-0110: 00",//勘验时间
			"investigationPlace": "湖里校区110号",//勘验地点
			"investigator": "张三、李四",//勘验人
			"lrr": "张三",//录入人
			"lrsj": "2015-01-0114: 00",//录入时间
			"sfsc": "1",//是否审查  1-已审查，0-未审查
			"sfhg": "1",//是否合格 1-合格，0-不合格
			"sfzg": "1",//是否整改 1-已整改，0-未整改
			"picNum": 20,//照片数量
			"tz": [1,2],//通知  第一个参数为短信数量，第二个参数为站内消息数量
			"fasj": "2016-08-1812: 25: 20",//发案时间
			"kysy": "xxx",//勘验事由
			"kyjcqk": "xxx"//勘验检查情况
		}
	],
    "pages": null,
    "operates": null
}
```

### 二、进入审查 查询需要审查照片信息接口

点击审查按钮时触发

#### API路径 

```http
http://localhost:8090/api/1/qualityCheck/xczp/_edit
```

后端格式为`/api/{recordLog}/qualityCheck/xczp/_edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "investigationNo":""//勘验编号
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
			"id": "B225A49283DA496C83AA79905C892EA2", //该组照片的id
			"picType": "现场图", //该组照片描述
			"picNum": 3,//该组照片数量
			"pics": [
				{
					"rownum": "1",
					"id": "B9F3FB8F562D48988E97584C8612E7FC",//需要审查的照片id
					"pId": "B225A49283DA496C83AA79905C892EA2",//照片组的id
					"base64": "",//照片的base64
					"desc": "平面示意图"//照片的描述
				}
			]
		}
	]，
    "pages": null,
    "operates": null
}
```

### 三、进入查看 查询审查的照片结果接口

点击查看按钮时触发

#### API路径 

```http
http://localhost:8090/api/1/qualityCheck/xczp/view
```

后端格式为`/api/{recordLog}/qualityCheck/xczp/view`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "investigationNo":""//勘验编号
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
			"id": "B225A49283DA496C83AA79905C892EA2",
			"picType": "现场图", //照片组描述、类型
			"picNum": 3,//照片数量
			"pics": [ //照片list
				{
					"rownum": "1",
					"id": "B9F3FB8F562D48988E97584C8612E7FC",//照片id
					"base64": "",//照片的base64
					"desc": "平面示意图",//照片的描述
					"result": "1"//照片审查的结果 1-合格，0-不合格
				}
			]
		}
	],
    "pages": null,
    "operates": null
}
```

### 四、页面审查保存接口

进入审查页面后，保存时触发

#### API 路径

```http
http://localhost:8090/api/1/qualityCheck/xczp/edit
```

后端格式为`/api/{recordLog}/qualityCheck/xczp/edit`,其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

`list`的值为认定为重复现场或者非重复现场的勘验id
**jsonStr:**
```json
{
    "investigationNo":"K1101126644646313233"  //审查的勘验编号
    "picList": [   //审查照片list
        {
			"id":"", //审查的照片的id
			"type":"1" //该照片审查结果 1-合格，0-不合格
		}
    ]
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```