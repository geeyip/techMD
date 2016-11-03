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
    "jqNo":"35021120160504500002",//警情编号
    "createDateStr":"2015-01-02 10:00:03",//反馈时间
    "zaMeans":"01,05"//作案手段
}
//其余字段可到FeedInfo类里查询
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":"","data":null,"pages":null,"operates":null}


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
    "appointNo":"35021120160504500002",//指派编号:警情/案件编号
    "ryNames":"454,张三",// 技术人员姓名
    "ryIds":"bfed55b9feb3420e8a8028a26636c2e9,15c3339fd8174f59826328535a4df08a"//技术人员id
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":"","data":null,"pages":null,"operates":null}


###警情编号/报案人/已反馈/指派、反馈查看接口

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
