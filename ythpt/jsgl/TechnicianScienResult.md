##技术人员科研成果API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/technician/kycg/list
```

后端格式为`/api/{recordLog}/jsgl/technician/kycg/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": "",             //技术人员id
"startTimeStart": "",     //开始时间起始
"startTimeEnd": "",       //开始时间终止
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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",       // 科研成果id
"techId": "",                                   // 技术人员id
"startTimeStr": "",                             // 开始时间
"endTimeStr": "",                               // 结束时间
"workDetail": "",                               // 完成情况
"workRole":"",                                  // 本人作用
"workResult":"",                                // 完成效果
"workFileId":""                                 // 附件id
}
],
"pages": null,
"operates": null
}
```

### 新增科研成果信息接口

保存新增内容时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/kycg/add
```

后端格式为`/api/{recordLog}/jsgl/technician/kycg/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "techId": "28c7590816d34f04867c03b1ce1f73d6",   // 技术人员id
    "startTime": "",                                // 开始时间
    "endTime": "",                                  // 结束时间
    "workDetail": "1",                              // 完成情况
    "workRole":"",                                  // 本人作用
    "workResult":"",                                // 完成效果
    "workFileId":""                                 // 附件id
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

### 修改科研成果信息接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/kycg/science_info
```

后端格式为`/api/{recordLog}/jsgl/technician/kycg/science_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"techId": ""                        //技术人员id
"startTimeStr": "",                 //开始时间(string类型)
"endTimeStr": "",                   //结束时间(string类型)
"workResult": "",                   //完成情况及效果、获何奖励
"workRole": "",                     //本人起何作用
"workDetail": "",                   //完成本专业技术工作情况
"workFileId": "",                   //附件名称
}
],
"pages": null,
"operates": null
}
```

### 保存修改科研成果信息接口

保存修改内容时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/kycg/edit
```

后端格式为`/api/{recordLog}/jsgl/technician/kycg/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": "",
"techId": "",                            //技术人员id
"startTime": "",                         //开始时间
"endTime": "",                           //结束时间
"workResult": "",                        //完成情况及效果、获何奖励
"workRole": "",                          //本人起何作用
"workDetail": "",                        //完成本专业技术工作情况
"workFileId": "",                        //附件名称
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

### 删除科研成果信息接口

点击删除按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/technician/kycg/delete
```

后端格式为`/api/{recordLog}/jsgl/technician/kycg/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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



