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
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":{"dnaInfo":[],"caseInfo":[{"cno":"A3502127400002016051000",
"unit":"厦门市公安局祥平派出所","detail":"福建省厦门市同安区祥平街道霞煌路58号",
"hadate":"2016-05-13 00:00:00","cname":"陈茂生"}],"handPrintInfo":[],"footInfo":[],
"investigationInfo":[]},"pages":null,"operates":null}
```
