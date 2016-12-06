## 人员管理API文档

### 人员查询接口

#### API路径

```http
http://localhost:8095/api/0/workbench/person/list
```

后端格式为`/api/{recordLog}/workbench/person/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{"pcdName":"SP_INT_API_SEL_PERSON_ALL",//存储过程名
 "pcdParamValMap":
{"pno":"aaa","birday":"2015-01-02", "idcard":"cc", "sex":"1","name":"tet","place":"350200000000"},
"begin":"1", "end":"200"}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":[],"pages":null,"operates":null}
```


### 人员详细页面接口

#### API路径

```http
http://localhost:8095/api/0/workbench/person/person_Info
```

后端格式为`/api/{recordLog}/workbench/person/person_Info，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```json
pno:R3501222916002010080037
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":{"perFootPrint":[],"jzInfo":[],"hitInfo":null,"falsePerson":
[{"ryzt":"未抓获","sfzh":"522624197906082612","sex":null,"pno":"R3506272305002009100007","lrsj":"1899-12-30 09:00:00",
"ryxm":"杨通刚","hjd":"贵州省三穗县良上乡上寨村土地塘组"},{"ryzt":"未抓获","sfzh":"522624197906082612","sex":null,
"pno":"R3506272305002009120001","lrsj":"2009-12-07 09:31:39","ryxm":"杨通刚","hjd":"贵州省三穗县良上乡上寨村土地塘组"}],
"perDna":[],"perHandPrint":[],"personInfo":[{"edulevel":"文盲","unit":"（无）","phone":"（无）","sex":"男",
"alias":"（无）","national":"中国","name":"杨通刚","pdetail":"（无）","idcard":"522624197906082612",
"hdetail":"贵州省三穗县良上乡上寨村土地塘组","nation":"苗族"}]},"pages":null,"operates":null}
```

