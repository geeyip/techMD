##环境管理API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/jsgl/environment/manage/list
```

后端格式为`/api/{recordLog}/jsgl/environment/manage/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "departments": "", //科室
  "laboratory": "", //实验室房号
  "charger": "",  //科技术负责人
  "createDateStrBegin": "",  //日期开始
  "createDateStrEnd": "",  //日期结束
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
			"rn": "1",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"departments"://科(室)（提供字典）,
			"laboratory"://实验室房号  "",
			"charger"://科技术负责人 "",
            "technology"://技术要求
            "environmentDate"://日期 "",
			"createPid":// 创建人"",
			"createDate"://创建时间 "",
			"modifyPid"://修改人 "",
			"modifyDate"://修改时间 "",
		}
    ],
    "pages": null,
    "operates": null
}
```


### 新增弹窗

点击新增保存按钮时触发

#### API路径

```http
http://localhost:8080/api/0/jsgl/environment/manage/add
```

后端格式为`/api/{recordLog}/jsgl/environment/manage/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "departments"://科(室)：（提供字典）,
    "laboratory"://实验室房号  "",
    "charger"://科技术负责人 "",
    "technology"://技术要求
    "environmentDate"://日期 "",
  }
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data":null,
    "pages": null,
    "operates": null
}
```

### 修改弹窗

点击修改保存按钮时触发

#### API路径

```http
http://localhost:8080/api/0/jsgl/environment/manage/edit
```

后端格式为`/api/{recordLog}/jsgl/environment/manage/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "id"://数据id,
    "departments"://科(室)：（提供字典）,
    "laboratory"://实验室房号  "",
    "charger"://科技术负责人 "",
    "technology"://技术要求
    "environmentDate"://日期 "",
  }
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data":null,
    "pages": null,
    "operates": null
}
````

### 删除操作

点击删除按钮时触发

#### API路径

```http
http://localhost:8080/api/0/jsgl/environment/manage/delete
```

后端格式为`/api/{recordLog}/jsgl/environment/manage/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "id": "", //删除信息id
  }
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data":null,
    "pages": null,
    "operates": null
}
````

### 导出操作

点击导出按钮时触发

#### API路径

```http
http://localhost:8080/api/0/jsgl/environment/manage/export
```

后端格式为`/api/{recordLog}/jsgl/environment/manage/export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{

  }
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data":null,
    "pages": null,
    "operates": null
}
````

### 科室自定义字典


#### API路径

```http
http://localhost:8080/api/0/jsgl/environment/manage/org
```

后端格式为`/api/{recordLog}/jsgl/environment/manage/org`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{

  }
```

#### 返回值格式

```json
{
    "flag": 1,
    "totalCount": null,
    "msg": null,
    "data":[
           		{
           			"key"://单位代码 "",
           			"value"://单位名称 "",
           		}
               ],
    "pages": null,
    "operates": null
}
````