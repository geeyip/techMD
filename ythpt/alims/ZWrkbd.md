##指纹入库比对API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/alims/zwrkbd/list
```

后端格式为`/api/{recordLog}/alims/zwrkbd/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
    "wzqk": "", //物证情况  有物证：0，有现场指纹：1
    "ajlb": "", //案件类别
    "kysjStart": "",  //勘验时间开始
    "kysjEnd": "",   //勘验时间结束
    "jqbh": "", //警情编号
    "ajbh": "", //案件编号
    "jyaq": "", //简要案情
    "faqh": "", //发案区划
    "fadd": "", //发案地点
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
            "id": "DC3BE807E29C43DFAE58B12A4EA93D3A",  //现勘ID
            "ajbh": "A110145656985321323",        //案件编号
            "jqbh": "J110145656985321322",        //警情编号
            "ajmc": "XXX派出所",                  //案件名称
            "ajlb": "入室盗窃",                   // 案件类别
            "fasjStr": "2016-08-18",             // 发案时间String类型
            "fadd": "某某单位",                  //发案地点
            "kybh": "",                          //勘验编号
            "wzsl": "5",                         //物证数量 int
            "zms": "5",                          //指纹总枚数 int
            "rk": "3",                           //指纹入库数 int
            "bz":"2",                            //指纹比中数 int
            "kysjStr": "2016-08-18",             // 勘验时间String类型
            "kyr": '某某',                       //勘验人
            "xczt":''                            //现场状态
		}
    ],
    "pages": null,
    "operates": null
}
````

### 物证指纹关联接口

点击指纹入库比对按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/alims/zwrkbd/wzzwgl
```

后端格式为`/api/{recordLog}/alims/zwrkbd/wzzwgl`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
     "inveId" : '' //现勘ID
     "hjlx" : '' //痕迹/物证类型
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
                "wzbh": "W110145656985321323",       //物证编号
                "wzmc": "匕首",                       //物证名称
                "wzlx": "",                          //物证类型
                "photoStr": "",                      //物证照片
                "zwbh": "某某单位",                    //指纹编号
            }
        ],
        "pages": null,
        "operates": null
}
```

### 指纹比中页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/alims/zwbd/list
```

后端格式为`/api/{recordLog}/alims/zwbd/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"sfrk": "", //指纹入库状态  1-已入库 0-未入库
"sfbz": "", //指纹比对状态  1-比中 0-未比中
"zwbh": "",  //指纹编号
"ajbh": "",  //案件编号
"kybh": "",  //勘验编号
"ajmc": "",  //案件名称
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
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",  //指纹id
"zwbh": "ZA110145656985321323",            //案件编号
"ajbh": "A110145656985321322",             //警情编号
"kybh": "",                                //案件名称
"ajmc": "x",                               //案件类别
"sfrk": "0",                               //是否入库 1-已入库 0-未入库
"sfbz": "1",                               //是否比中 1-比中 0-未比中
}
],
"pages": null,
"operates": null
}
````
