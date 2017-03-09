## 案事件勘验API文档

### 警情反馈接口

#### API路径

```http
http://localhost:8095/api/1/workbench/jqxx/feed
```

后端格式为`/api/{recordLog}/workbench/jqxx/feed`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "jcjSystemId":"PC021120160504500002",//警情编号
    "createDateStr":"2015-01-02 10:00:03",//反馈时间
    "zaMeans":"01,05"//作案手段
}
//其余字段可到FeedInfo类里查询
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":"","data":null,"pages":null,"operates":null}
```

### 警情/案件指派接口

#### API路径

```http
http://localhost:8095/api/1/workbench/jqxx/appoint
```

后端格式为`/api/{recordLog}/workbench/jqxx/appoint`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "type":"1",//指派类型：1警情，2案件
    "appointNo":"PC021120160504500002",//指派编号:警情id/案件编号
    "ryNames":"454,张三",// 技术人员姓名
    "ryIds":"bfed55b9feb3420e8a8028a26636c2e9,15c3339fd8174f59826328535a4df08a"//技术人员id
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":"","data":null,"pages":null,"operates":null}
```

###警情编号/报案人/已反馈/反馈查看接口

#### API路径

```http
http://localhost:8095/api/0/workbench/jqxx/jq_info
```

后端格式为`/api/{recordLog}/workbench/jqxx/jq_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "systemid":"PCS3500201605040000002025114343"//主键
}
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null}
//date数据具体参考JqInfo类
```

###案事件数量接口

#### API路径

```http
http://localhost:8095/api/0/workbench/jqxx/count
```

后端格式为`/api/{recordLog}/workbench/jqxx/count`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```
无传入参数
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null,
"data":{"jqdcl_wwc":0,"jqzp_yzp":0,"yqwkaj_wzp":0,"ajzp_wzp":0,"jqdcl_wc":0,
        yqwkaj_yzp":0, "jqzp_wzp":0,"ajdcl_wc":0,"ajdcl_wwc":0,"ajzp_yzp":0},
"pages":null,"operates":null}
```

###指派列表接口

#### API路径

```http
http://localhost:8095/api/0/workbench/jqxx/appoint_info
```

后端格式为`/api/{recordLog}/workbench/jqxx/appoint_info，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```
无传入参数
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null,"data":[],"pages":null,"operates":null}
//data中的list字段：id 技术人员编号 trueName 真实姓名 kys 勘验数 mobilephoneNo 电话
```


###新增警情接口

#### API路径

```http
http://localhost:8095/api/0/workbench/jqxx/add
```

后端格式为`/api/{recordLog}/workbench/jqxx/add，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
$post('http://localhost:8090/api/0/workbench/jqxx/add', {
	slBjslh: '141221',
	sljjsj: '2016-05-09',
	gxdwdm: '350200000000',
	ab: 'ccc',
	sljjry: '李四',
	fadd: '海越大厦',
	zyaq: '抢夺案',
	sspq: '01',
	appointUnit: '350200000000',
	appointTime: '2016-05-09'
},
function(res) {
	log(res)
},
true)
```

#### 返回值格式
```json
{
	flag: 1,
	totalCount: 0,
	msg: null,
	data: null,
	pages: null…
}
```

* 案事件勘验改造接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/ky_aj_jcjxx/list', {
	"pcdName": "SP_INT_API_SEL_REC_SCN_ALL",
	"pcdParamValMap": {"recno":"J350182720000201401000001"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"rectime": "2014-01-01 02:06:25",
		"recunit": "350182000000",
		"phtamt": null,
		"evidamt": null,
		"collamt": null,
		"haptime": null,
		"sceneno": null,
		"caseno": null,
		"casekd": null,
		"invest": null,
		"rownum": 1,
		"hapdetl": null,
		"acctunit": null,
		"fileno": "T350200201703070013730287",
		"recno": "J350182720000201401000001",
		"pictamt": null,
		"scetime": null,
		"casename": null,
		"sceflag": "0",
		"scesta": null,
		"accttime": null
	}],
	"pages": null,
	"operates": null
}
```

```java
字段说明：
案事件勘验查询结果集说明：{"rectime":"出警时间、接警时间","recunit":"接警单位","phtamt":"现场照片数量","evidamt":"痕迹物证","collamt":"提取物品","haptime":"发案时间","sceneno":"现勘编号","caseno":"案件编号","casekd":"案件类别","rownum":"排序序号","invest":"勘验人","hapdetl":"发案地点","acctunit":"受理单位","fileno":"案件档案号","recno":"接警编号","pictamt":"现场图数量","scetime":"勘验时间","casename":"案件名字","sceflag":"勘验是否合格，‘0’为不合格，‘1’为合格","scesta":"勘验状态","accttime":"受理时间"}
案事件勘验查询参数说明：{"secflag":"是否勘验","unitflag":"单位标志 1表示接警单位，2表示受理单位","recby":"接警人","caseno":"案件编号","acctmin":"受理时间初值","casekd":"案件类别","unit":"接警或受理单位","acctmax":"受理时间终值","recno":"警情编号","rectmin":"接警时间初值","rectmax":"接警时间终值"}
```



