##耗材管理API文档

### 耗材管理页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/asset/invitation/list
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "invitationName": "",     //耗材名称
    "invitationCode": "",     //耗材编号
    "storagePeron": "",       //保管人
    "storageDate": "",        //入库时间
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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"storageDateStr": "",                         //入库时间
"totalNumber": "",                            //耗材数量
"storagePerson": "",                          //保管人
"storagePersonId": "",                        //保管人id
"storageNumber": "",                          //在库数量
"infoRemark": "",                             //备注
}
],
"pages": null,
"operates": null
}
```

### 新增耗材管理信息接口

点击新增按钮后保存时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/add
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"storageDate": "",                            //入库时间
"totalNumber": "",                            //耗材数量
"storagePerson": "",                          //保管人
"storagePersonId": "",                        //保管人id
"infoRemark": "",                             //备注
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

### 修改耗材管理信息接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/invitation_info
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/invitation_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"storageDate": "",                            //入库时间
"totalNumber": "",                            //耗材数量
"storagePerson": "",                          //保管人
"storagePersonId": "",                        //保管人id
"infoRemark": "",                             //备注
}
],
"pages": null,
"operates": null
}
```

### 保存修改耗材管理信息接口

点击修改按钮后保存时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/edit
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"storageDate": "",                            //入库时间
"totalNumber": "",                            //耗材数量
"storagePerson": "",                          //保管人
"storagePersonId": "",                        //保管人id
"infoRemark": "",                             //备注
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

### 删除耗材管理信息接口

点击删除按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/delete
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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

### 查看耗材管理信息接口

点击耗材编号时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/invitation_info
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/invitation_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"storageDate": "",                            //入库时间
"totalNumber": "",                            //耗材数量
"storagePerson": "",                          //保管人
"storagePersonId": "",                        //保管人id
"infoRemark": "",                             //备注
}
],
"pages": null,
"operates": null
}
```

### 领用耗材接口

点击领用按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/invitation_info
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/invitation_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"storageDate": "",                            //入库时间
"totalNumber": "",                            //耗材数量
"storagePerson": "",                          //保管人
"storagePersonId": "",                        //保管人id
"storageNumber":"",                           //在库数量
"infoRemark": "",                             //备注
}
],
"pages": null,
"operates": null
}
```

### 保存领用耗材信息接口

点击保存按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/record_add
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/record_add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"invitationId": "DC3BE807E29C43DFAE58B12A",   //耗材信息id
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"receiveDate": "",                            //领用时间
"receiveNum": "",                             //领用数量
"receiveUser": "",                            //领用人
"techId": "",                                 //领用人id
"recordRemark": "",                           //备注
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

### 耗材管理信息导出excel接口

点击导出Excel按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/export
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求


#### 传入参数格式


#### 返回值格式



### 耗材领取记录页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/asset/invitation/record_list
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/record_list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"invitationName": "",     //耗材名称
"invitationCode": "",     //耗材编号
"receiveUser": "",       //领用人
"receiveDate": "",        //领用时间
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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
"invitationName": "",                         //耗材名称
"invitationCode": "",                         //耗材编号
"receiveDateStr": "",                         //领用时间
"receiveNum": "",                             //领用数量
"receiveUser": "",                            //领用人
"techId": "",                                 //领用人id
"recordRemark": "",                           //备注
}
],
"pages": null,
"operates": null
}
```

### 耗材领取记录导出excel接口

点击导出Excel按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/asset/invitation/record_export
```

后端格式为`/api/{recordLog}/jsgl/asset/invitation/record_export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求


#### 传入参数格式


#### 返回值格式
