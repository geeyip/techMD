##检验方法管理API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/jsgl/calibration/manage/query
```

后端格式为`/api/{recordLog}/jsgl/calibration/manage/query`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "perofession": "", //使用专业
  "standards": "", //检测标准(方法)
  "calibrationNo": "",  //编号(含年号)
  "publisher": "",  //编制者/发布者
  "validFlag": "",  //是否有效
  "newFlag": "", //是否为最新
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
			"perofession"://使用专业（提供字典）,
			"standards"://检测标准(方法)  "",
			"calibrationNo"://检测编号 "",
            "publisher"://发布人
            "validFlag"://是否有效 "",
            "newFlag"://是否最新
            "remark"://说明
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
http://localhost:8080/api/0/jsgl/calibration/manage/add
```

后端格式为`/api/{recordLog}/jsgl/calibration/manage/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "perofession"://使用专业（提供字典）,
    "standards"://检测标准(方法)  "",
    "calibrationNo"://检测编号 "",
    "publisher"://发布人
    "validFlag"://是否有效 "",
    "newFlag"://是否最新
    "remark"://说明
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
http://localhost:8080/api/0/jsgl/calibration/manage/edit
```

后端格式为`/api/{recordLog}/jsgl/calibration/manage/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "perofession"://使用专业（提供字典）,
    "standards"://检测标准(方法)  "",
    "calibrationNo"://检测编号 "",
    "publisher"://发布人
    "validFlag"://是否有效 "",
    "newFlag"://是否最新
    "remark"://说明
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
http://localhost:8080/api/0/jsgl/calibration/manage/delete
```

后端格式为`/api/{recordLog}/jsgl/calibration/manage/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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
http://localhost:8080/api/0/jsgl/calibration/manage/export
```

后端格式为`/api/{recordLog}/jsgl/calibration/manage/export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
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