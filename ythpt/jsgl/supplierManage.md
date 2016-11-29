##供应商管理API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/supplier/list
```

后端格式为`/api/{recordLog}/jsgl/supplier/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "supplierName": "",     //供应商名称
    "supplierContent": "",  //供应内容
    "contactPerson": "",    //联系人
    "vocation": "",         //职务
    "telephone": "",        //电话/手机
    "address": "",          //地址
    "postcode": "",         //邮编
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
            "supplierName": "",                         //供应商名称
            "supplierContent": "",                      //供应内容
            "contactPerson": "",                        //联系人
            "vocation": "",                             //职务
            "telephone": "",                            //电话/手机
            "address": "",                              //地址
            "postcode": "",                             //邮编
            "remark": "",                               //备注
        }
    ],
    "pages": null,
    "operates": null
}
```

### 新增供应商信息接口

点击新增按钮后保存时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/supplier/add
```

后端格式为`/api/{recordLog}/jsgl/supplier/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "supplierName": "",                         //供应商名称
    "supplierContent": "",                      //供应内容
    "contactPerson": "",                        //联系人
    "vocation": "",                             //职务
    "telephone": "",                            //电话/手机
    "address": "",                              //地址
    "postcode": "",                             //邮编
    "remark": "",                               //备注
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

### 修改供应商信息接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/supplier/supplier_info
```

后端格式为`/api/{recordLog}/jsgl/supplier/supplier_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
            "supplierName": "",                         //供应商名称
            "supplierContent": "",                      //供应内容
            "contactPerson": "",                        //联系人
            "vocation": "",                             //职务
            "telephone": "",                            //电话/手机
            "address": "",                              //地址
            "postcode": "",                             //邮编
            "remark": "",                               //备注
        }
    ],
    "pages": null,
    "operates": null
}
```

### 保存修改供应商信息接口

点击修改按钮后保存时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/supplier/edit
```

后端格式为`/api/{recordLog}/jsgl/supplier/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "supplierName": "",                         //供应商名称
    "supplierContent": "",                      //供应内容
    "contactPerson": "",                        //联系人
    "vocation": "",                             //职务
    "telephone": "",                            //电话/手机
    "address": "",                              //地址
    "postcode": "",                             //邮编
    "remark": "",                               //备注
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

### 删除供应商信息接口

点击删除按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/supplier/delete
```

后端格式为`/api/{recordLog}/jsgl/supplier/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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

### 查看供应商信息接口

点击供应商名称时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/supplier/supplier_info
```

后端格式为`/api/{recordLog}/jsgl/supplier/supplier_info`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
        "supplierName": "",                         //供应商名称
        "supplierContent": "",                      //供应内容
        "contactPerson": "",                        //联系人
        "vocation": "",                             //职务
        "telephone": "",                            //电话/手机
        "address": "",                              //地址
        "postcode": "",                             //邮编
        "remark": "",                               //备注
    }
],
"pages": null,
"operates": null
}
```

### 供应商信息导出excel接口

点击导出Excel按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/jsgl/supplier/export
```

后端格式为`/api/{recordLog}/jsgl/supplier/export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求


#### 传入参数格式


#### 返回值格式



