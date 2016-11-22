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
  "ybslsjBegin": "", //样本受理时间开始
  "ybslsjEnd": "", //样本受理时间结束
  "ajbh": "",  //案件编号
  "ajmc": "",  //案件名称
  "yblx": "",  //样本类型
  "bdzt": "", //比对状态
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
			"caseNo"://案件编号  "",
			"caseName"://案件名称 "",
            "bdzt"://比对状态代码
            "jyaq"://简要案情 "",
            "slsj"://受理时间
            "slr"://受理人
			"sjsj"://送检时间 "",
			"sjr"://送检人 "",
			"jysj"://检验时间 "",
			"jyr"://检验人 "",
			"sampleNo"://条形码"",
			"evidenceNo"://物证编号 "",
			"sampleLabNo"://DNA检材编号 ,
			"sampleName"://样本名称,
			"flag"://类型 person object
			"sampleType"://样本类型代码（提供字典）,
			"fullname"://人员姓名
			"personType"://人员类型
			"gender"://性别
			"cardId"://身份证号
			"finishAt"://结束时间（暂为lims中审核时间
			"submittime"://入库时间
			"perLy"://人员来源
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
  "flag":""//查询类别 "object"
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
			"matchNo"://目标编号(物证编号,人员DNA样本编号),
			"dataType":// 1:填充表格后半段 ; 0:填充表格前半段
			"aaEvidenceNo"://// dataType=0 物证编号, dataType=1 比中物证编号 ,
			"aaSampleName":// dataType=0 物证名称, dataType=1 比中物证名称 ,
			"aaSampleLabNo"：//DNA检材编号,
            "matchType"://比中类型（案案、案人、人案、人人） ,
			"aaCaseNo":// dataType=0 案件编号, dataType=1 比中案件编号 ,
			"aaCaseName"://dataType=0 案件名称, dataType=1 比中案件名称 ,
		}
    ],
    "pages": null,
    "operates": null
}
```

### 物证已比中弹窗人案table

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/alims/DNA/view/all
```

后端格式为`/api/{recordLog}/alims/DNA/view/all`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "evidenceNo": "", //物证编号
  "flag":""//查询类别 "object" "person"
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
			"matchNo"://目标编号(物证编号,人员DNA样本编号),
			"matchType"://比中类型（案案、案人、人案、人人） ,
			"evidenceNo"://物证编号
			"sampleLabNo"://DNA检材编号,
            "caseNo"://案件编号，
            "sampleName"://样本名称
            "caseName"://案件名称
			"arRybh"://比中人员编号 ,
			"arRperName"://人员姓名 "",
			"arPerPaper"://人员身份证号码 "",
		}
    ],
    "pages": null,
    "operates": null
}
````

### 物证已比中弹窗人人table

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
  "flag":""//查询类别 "person"
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
			"matchNo"://目标编号(物证编号,人员DNA样本编号),
			"dataType":// 1:填充表格后半段 ; 0:填充表格前半段
			"matchType"://比中类型（案案、案人、人案、人人） ,
			"bzEampleLabNo"://DNA检材编号,
			"caseNo"://案件编号，
			"bzEvidenceNo"://比中物证编号
			"bzSampleName"://样本名称
			"caseName"://案件名称
			"arRybh"://比中人员编号 ,
			"arRperName"://人员姓名 "",
			"arPerPaper"://人员身份证号码 "",
		}
    ],
    "pages": null,
    "operates": null
}
````