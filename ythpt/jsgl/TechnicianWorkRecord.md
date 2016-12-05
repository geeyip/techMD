##技术人员工作履历API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/technician/gzll/list
```

后端格式为`/api/{recordLog}/jsgl/technician/gzll/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": "",              //技术人员id
"workUnit": "",             //工作单位
"workPost": "",             //职务/职称
"startTimeStart": "",      //开始时间起始
"startTimeEnd": ""         //开始时间终止
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
"rownum": "1",
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",       // 工作履历id
"techId": "",                                   // 技术人员id
"workUnit": "",                                 // 工作单位
"workContent": "",                              // 从事工作
"workPost": "",                                 // 职务/职称
"startTimeStr": "",                             // 开始时间
"endTimeStr": "",                               // 结束时间
}
],
"pages": null,
"operates": null
}
```

### 新增工作履历信息接口

保存新增内容时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/gzll/add
```

后端格式为`/api/{recordLog}/jsgl/technician/gzll/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": "",                                   // 技术人员id
"workUnit": "",                                 // 工作单位
"workContent": "",                              // 从事工作
"workPost": "",                                 // 职务/职称
"startTime": "",                                // 开始时间
"endTime": "",                                  // 结束时间
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

### 修改工作履历信息接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/gzll/work_info
```

后端格式为`/api/{recordLog}/jsgl/technician/gzll/work_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": "",
"techId": ""             //技术人员id
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
"id": "",
"techId": "",                                   // 技术人员id
"workUnit": "",                                 // 工作单位
"workContent": "",                              // 从事工作
"workPost": "",                                 // 职务/职称
"startTimeStr": "",                             // 开始时间
"endTimeStr": "",                               // 结束时间
}
],
"pages": null,
"operates": null
}
```

### 保存修改工作履历信息接口

保存修改内容时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/gzll/edit
```

后端格式为`/api/{recordLog}/jsgl/technician/gzll/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": "",
"techId": "",                                   // 技术人员id
"workUnit": "",                                 // 工作单位
"workContent": "",                              // 从事工作
"workPost": "",                                 // 职务/职称
"startTime": "",                                // 开始时间
"endTime": "",                                  // 结束时间
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

### 删除工作履历信息接口

点击删除按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/gzll/delete
```

后端格式为`/api/{recordLog}/jsgl/technician/gzll/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": "",
"techId": ""             //技术人员id
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
