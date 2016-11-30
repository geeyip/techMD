##技术人员论文著作情况API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/technician/lwzzqk/list
```

后端格式为`/api/{recordLog}/jsgl/technician/lwzzqk/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": ""，              //技术人员id
"paperTitle": "",          //论文、著作标题
"publishName": ""          //刊物名称
"publishUnit": "",         //刊物(论文交流)主办单位
"publishDateStart": ""     //发布时间开始
"publishDateEnd": ""       //发布时间结束
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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",       // 论文情况id
"techId": "",                                   // 技术人员id
"paperTitle",                                   // 论文著作标题
"paperAuthor",                                  // 作者
"publishName",                                  // 刊物名称
"publishDateStr",                               // 发布出版时间
"publishRank",                                  // 排名
"publishNo",                                    // 刊号
"publishUnit",                                  // 刊物(论文交流)主办单位
}
],
"pages": null,
"operates": null
}
```

### 新增论文情况信息接口

保存新增内容时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/lwzzqk/add
```

后端格式为`/api/{recordLog}/jsgl/technician/lwzzqk/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": "",                                   // 技术人员id
"paperTitle",                                   // 论文著作标题
"paperAuthor",                                  // 作者
"publishName",                                  // 刊物名称
"publishDate",                                  // 发布出版时间
"publishRank",                                  // 排名
"publishNo",                                    // 刊号
"publishUnit",                                  // 刊物(论文交流)主办单位
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

### 修改论文情况信息接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/lwzzqk/paper_info
```

后端格式为`/api/{recordLog}/jsgl/technician/lwzzqk/paper_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
"paperTitle",                                   // 论文著作标题
"paperAuthor",                                  // 作者
"publishName",                                  // 刊物名称
"publishDateStr",                               // 发布出版时间
"publishRank",                                  // 排名
"publishNo",                                    // 刊号
"publishUnit",                                  // 刊物(论文交流)主办单位
}
],
"pages": null,
"operates": null
}
```

### 保存修改论文情况信息接口

保存修改内容时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/lwzzqk/edit
```

后端格式为`/api/{recordLog}/jsgl/technician/lwzzqk/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
"paperTitle",                                   // 论文著作标题
"paperAuthor",                                  // 作者
"publishName",                                  // 刊物名称
"publishDate",                                  // 发布出版时间
"publishRank",                                  // 排名
"publishNo",                                    // 刊号
"publishUnit",                                  // 刊物(论文交流)主办单位
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

### 删除论文情况信息接口

点击删除按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/lwzzqk/delete
```

后端格式为`/api/{recordLog}/jsgl/technician/lwzzqk/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
