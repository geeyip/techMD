##串并案管理API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/0/yppt/cba/manage/query
```

后端格式为`/api/{recordLog}/yppt/cba/manage/query`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
#### 传入参数格式
**jsonStr:**
```json
{
  "createDateBegin": "", //串并时间开始
  "createDateEnd": "", //串并时间结束
  "cbyj": "", //串并依据 指纹/足迹/DNA/手段特点 (直接传中文)
  "cblyCn": "", //串并来源 字典：CBZTDM
  "cbaid": "",  //串并号
  "cbmc": "",  //串并名称
  "cblb": "", //串并类别 字典：CBLBDM
  "paNum": "",  //是否存在破案 1：存在破案 0：不存在破案
  "cbdw": "", //串并单位 字典：GXSDM
  "checkStateProv": "",//省厅审核情况 字典：SHZTDM 对应值
  "checkState": "", //市局审核情况 字典：SHZTDM 对应值
  "kno": "", //先看编号
  "caseNo": "", //案件编号
  "persNo": "", //人员编号
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
			"id": //数据id"",
			"cbaid"://串并案编号,
			"hbid"://合并串编号"",
			"cbmc"://串并名称  "",
			"cblbarray"://串并类别 字符串数组"",
			"cbyj"://串并依据 "",
            "createDateStr"://首串时间
			"xcsj"://续串时间 "",
			"cbnum"://串并案件数 "",
            "rynum"://串并人员数量
			"paNum"://破案数 "",
			"jspaNum"://技术破案数
            "cbdwdm"://串并单位
			"cbdw"://串并单位中文 "",
			"checkStateProv"://省级审核状态,
			"checkDateProv"://省级审核时间,
			"checkPidProv"://省级审核人员
			"checkState"://市级审核状态
			"checkDate"://市级审核时间
			"checkPid"://市级审核人员
			"cblyCn"://串并来源中文 ,
		}
    ],
    "pages": null,
    "operates": null
}
```
### 串并案查看接口

点击查看按钮时触发

#### API路径

```http
openIE:
path: localData.get('sysParam').xjptAddress + '/bunchDetailForView.action?cbaid='+//串并案编号
```

### 串并案修改接口

点击修改按钮时触发

#### API路径

```http
openIE:
path: localData.get('sysParam').xjptAddress + '/pages/singleJhLogin.action?jh='+localData.get('currentUser').policeNo+'&cbaId='+//串并案编号