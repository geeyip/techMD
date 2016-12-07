## 案件查询API文档

### 案件查询接口

#### API路径

```http
http://localhost:8095/api/0/workbench/case/list
```

后端格式为`/api/{recordLog}/workbench/case/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{"pcdName":"SP_INT_API_SEL_CASE_ALL",
"pcdParamValMap":{"cno":"aaa","maxdate":"2015-01-02","mindate":"2015-01-02",
"idcard":"cc","detail":"ccc","summary":"kk","kind":"452600","name":"tet","place":"350200000000"},
 "begin":"1", "end":"200"}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":[],"pages":null,"operates":null}
```

### 案件详细页面接口

#### API路径

```http
http://localhost:8095/api/0/workbench/case/case_Info
```

后端格式为`/api/{recordLog}/workbench/case/case_Info，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```json
cno:A3502127400002016051000
pcdName:SP_INT_API_SEL_CASE_INFO//值不为空时返回单块信息
```

### 存储过程枚举
```json
SP_INT_API_SEL_CASE_INFO("SP_INT_API_SEL_CASE_INFO", "caseInfo", "查询案件基本信息"), //一体化查询案件基本信息
SP_INT_API_SEL_REL_CASE_SCENE("SP_INT_API_SEL_REL_CASE_SCENE", "investigationInfo", "查询勘验现场信息"),//一体化查询勘验现场信息
SP_INT_API_SEL_REL_CASE_HAND("SP_INT_API_SEL_REL_CASE_HAND", "handPrintInfo" , "查询提取现场指纹"),//一体化查询提取现场指纹
SP_INT_API_SEL_REL_CASE_DNA("SP_INT_API_SEL_REL_CASE_DNA", "dnaInfo", "查询提取现场DNA"),//一体化查询提取现场DNA
SP_INT_API_SEL_REL_CASE_FOOT("SP_INT_API_SEL_REL_CASE_FOOT", "footInfo", "查询提取现场足迹"),//一体化查询提取现场足迹
SP_CET_API_SEL_CASE_HIT_INFO("SP_CET_API_SEL_CASE_HIT_INFO", "hitInfo", "查询案件涉案比中情况"),//一体化查案询件涉案比中情况
```

#### 返回值格式

```json
{
	"flag": 1,
	"totalCount": 0,
	"msg": null,
	"data": {
		"dnaInfo": [{
			"position": "a22",
			"unit": "a45",
			"time": "a27",
			"dno": "a90",
			"name": "a82",
			"type": "a88",
			"user": "a74",
			"labno": "a98"
		}],
		"hitInfo": [{
			"ryly": "a26",
			"lrsj": "a2",
			"hjd": "a78",
			"ryzt": "a63",
			"sfzh": "a80",
			"pno": "a74",
			"lx": "a10",
			"ryxm": "a73"
		}],
		"caseInfo": [{
			"summary": "a23",
			"unit": "a65",
			"rno": "a4",
			"detail": "a99",
			"status": "a1",
			"hadate": "2016-12-06",
			"cno": "a37",
			"place": "a55",
			"user": "a74",
			"redate": "2016-12-06",
			"kind": "a10",
			"cname": "a38",
			"sodate": "2016-12-06"
		}],
		"handPrintInfo": [{
			"position": "a28",
			"unit": "a58",
			"detail": "a55",
			"time": "a72",
			"colltime": "a59",
			"hno": "a54",
			"user": "a65",
			"kind": "a89"
		}],
		"footInfo": [{
			"position": "a36",
			"unit": "a69",
			"colltime": "a88",
			"collby": "a49",
			"type": "a16",
			"fno": "a37"
		}],
		"investigationInfo": [{
			"lotude": "a2",
			"location": "a62",
			"latude": "a69",
			"means": "a38",
			"way": "a91",
			"addr": "a24",
			"charcs": "a28",
			"content": "a7",
			"unit": "a78",
			"time": "a87",
			"order": "a33",
			"name": "a95",
			"value": "a11",
			"critime": "a38",
			"kno": "a68",
			"user": "a58"
		}]
	},
	"pages": null,
	"operates": null
}
```
