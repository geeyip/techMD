##DNA入库比对API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/alims/DNA/query
```

后端格式为`/api/{recordLog}/alims/DNA/query`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "ajlx": "", //案件类型
  "faqh": "", //发案区划 字典代码
  "ybslsjBegin": "", //样本受理时间开始
  "ybslsjEnd": "", //样本受理时间结束
  "ajbh": "",  //案件编号
  "ajmc": "",  //案件名称
  "yblx": "",  //样本类型
  "jyzt": "", //检验状态
  "bdzt": "", //比对状态
  "jqbh": "", //警情编号
  "kybh": "", //勘验编号
  "fadd": "", //发案地点
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
			"rn": "1",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"caseType"://案件类型代码（提供字典）,
			"sceneRegionalism"://发案区划代码 "",
			"caseNo"://案件编号  "",
			"caseName"://案件名称 "",
			"jyaq"://简要案情 "",
			"jqbh"://警情编号 "",
			"incerstigationNo"://勘验编号 "",
			"occurrCaroom"://发案地点 "",
			"sampleName"://样本名称/物证名称 "",
			"sampleNo"://条形码"",
			"evidenceNo"://物证编号 "",
			"sampleLabNo"://DNA检材编号 ,
			"sampleType"://样本类型代码（提供字典）,
			"slsj"://受理时间
			"tqsj"://提取时间
			"jyzt"://检验状态代码（提供字典）
			"bdzt"://比对状态代码（提供字典）
			"createUser"://录入员编号
			"createDatetime"://录入时间
			"updateUser"://修改人员编号
			"updateDatetime"://修改时间
		}
    ],
    "pages": null,
    "operates": null
}
```


### 物证已比中弹窗案案table

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/alims/DNA/view/evidence
```

后端格式为`/api/{recordLog}/alims/DNA/view/evidence`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "evidenceNo": "", //物证编号
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
			"rn": "1",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"matchNo"://案件类型代码（提供字典）,
			"matchType"://发案区划代码 ,
			"caseNo"://比中案件编号 ,
			"caseName"://比中案件名称 "",
			"sampleName"://比中物证名称 "",
		}
    ],
    "pages": null,
    "operates": null
}
```

### 物证已比中弹窗案案table

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/alims/DNA/view/person
```

后端格式为`/api/{recordLog}/alims/DNA/view/person`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "evidenceNo": "", //物证编号
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
			"rn": "1",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"matchNo"://案件类型代码（提供字典）,
			"matchType"://发案区划代码 ,
			"rybh"://比中人员编号 ,
			"perName"://人员姓名 "",
			"perPaper"://人员身份证号码 "",
		}
    ],
    "pages": null,
    "operates": null
}
```