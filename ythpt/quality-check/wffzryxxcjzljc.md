##违法犯罪人员采集质量检查API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/zcxt/illegal/personnel/query
```

后端格式为`/api/{recordLog}/zcxt/illegal/personnel/query`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "unitCode": "", //采集单位代码
  "createDateStrBegin": "",  //采集时间开始
  "createDateStrEnd": "",  //采集时间结束
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
			"unitCode"://单位代码 "",
            "unitName"://单位名称 "",
			"allnum"://采集数合计,
			"allpassnum"://采集数合格数  "",
			"allnopassnum"://采集数不合格数 "",
            "ninenum"://九类人员合计
            "ninepassnum"://九类人员合格数 "",
            "ninenopassnum"://九类人员不合格数
            "noninenum"://非九类人员合计
			"noninepassnum":// 非九类人员合格数"",
			"noninenopassnum"://非九类人员不合格数 "",
			"dnaCount"://人员DNA收讫入库情况 合计
            "dnaNanCount":// 人员DNA收讫入库情况 入库"",
            "dnaNvCount"://人员DNA收讫入库情况  收讫"",

		}
    ],
    "pages": null,
    "operates": null
}
```

### 导出操作

点击导出按钮时触发

#### API路径

```http
http://localhost:8080/api/0/zcxt/illegal/personnel/export
```

后端格式为`/api/{recordLog}/zcxt/illegal/personnel/export`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

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