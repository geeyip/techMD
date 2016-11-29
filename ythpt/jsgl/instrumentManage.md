##仪器管理API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/instrument/list
```

后端格式为`/api/{recordLog}/jsgl/instrument/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"instrumentName": "",       //仪器名称
"instrumentModel": "",      //规格型号
"manufacturer": "",         //生产厂家
"purchaseDateStart": "",    //购买时间开始
"purchaseDateEnd": "",      //购买时间结束
"instrumentCode": "",       //编号
"laboratory": "",           //实验室/房号
"responsiblePerson": "",    //责任人
"begin": 1,
"end": 200
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
"instrumentName": "",       //仪器名称
"instrumentModel": "",      //规格型号
"range": "",                //量程
"accuracy": "",             //准确度
"manufacturer": "",         //生产厂家
"purchaseDateStr": "",      //购买时间
"instrumentCode": "",       //编号
"laboratory": "",           //实验室/房号
"responsiblePerson": ""     //责任人
}
],
"pages": null,
"operates": null
}
```

### 新增仪器信息接口

点击新增按钮后保存时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/instrument/add
```

后端格式为`/api/{recordLog}/jsgl/instrument/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"instrumentName": "",       //仪器名称
"instrumentModel": "",      //规格型号
"range": "",                //量程
"accuracy": "",             //准确度
"manufacturer": "",         //生产厂家
"purchaseDate": "",         //购买时间
"instrumentCode": "",       //编号
"laboratory": "",           //实验室/房号
"responsiblePerson": ""     //责任人
}
```

#### 返回值格式

```json
{
"flag":1,
"totalCount":0,
"msg":null,
"data":null,
"pages":null,
"operates":null
}
```

### 修改仪器信息接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/instrument/instrument_info
```

后端格式为`/api/{recordLog}/jsgl/instrument/instrument_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": ""
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
"instrumentName": "",       //仪器名称
"instrumentModel": "",      //规格型号
"range": "",                //量程
"accuracy": "",             //准确度
"manufacturer": "",         //生产厂家
"purchaseDate": "",         //购买时间
"instrumentCode": "",       //编号
"laboratory": "",           //实验室/房号
"responsiblePerson": ""     //责任人
}
],
"pages": null,
"operates": null
}
```

### 保存修改仪器信息接口

点击修改按钮后保存时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/instrument/edit
```

后端格式为`/api/{recordLog}/jsgl/instrument/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"instrumentName": "",       //仪器名称
"instrumentModel": "",      //规格型号
"range": "",                //量程
"accuracy": "",             //准确度
"manufacturer": "",         //生产厂家
"purchaseDate": "",         //购买时间
"instrumentCode": "",       //编号
"laboratory": "",           //实验室/房号
"responsiblePerson": ""     //责任人
}
```

#### 返回值格式

```json
{
"flag":1,
"totalCount":0,
"msg":null,
"data":null,
"pages":null,
"operates":null
}
```

### 删除仪器信息接口

点击删除按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/instrument/delete
```

后端格式为`/api/{recordLog}/jsgl/instrument/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": ""
}
```


#### 返回值格式

```json
{
"flag":1,
"totalCount":0,
"msg":null,
"data":null,
"pages":null,
"operates":null
}
```

### 查看仪器信息接口

点击仪器名称时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/instrument/instrument_info
```

后端格式为`/api/{recordLog}/jsgl/instrument/instrument_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": ""
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
"instrumentName": "",       //仪器名称
"instrumentModel": "",      //规格型号
"range": "",                //量程
"accuracy": "",             //准确度
"manufacturer": "",         //生产厂家
"purchaseDate": "",         //购买时间
"instrumentCode": "",       //编号
"laboratory": "",           //实验室/房号
"responsiblePerson": ""     //责任人
}
],
"pages": null,
"operates": null
}
```

### 仪器信息导出excel接口

点击导出Excel按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/instrument/export
```

后端格式为`/api/{recordLog}/jsgl/instrument/export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求


#### 传入参数格式


#### 返回值格式



