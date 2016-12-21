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
     "inveId" : '现勘ID',
     "hjlx" : '痕迹/物证类型'
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
                "zwbh": "某某单位"                     //指纹编号
            }
        ],
        "pages": null,
        "operates": null
}

```

### 指纹比对页面查询接口

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
"sfbz": "1"                               //是否比中 1-比中 0-未比中
}
],
"pages": null,
"operates": null
}
````

### 指纹比中审核页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/alims/zwbzsh/list
```

后端格式为`/api/{recordLog}/alims/zwbzsh/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"sjzt": "",       //数据状态
"bzfs": "",       //比对方式
"xczwbh": "",     //现场指纹编号
"szzwbh": "",    //十指指纹编号
"ajbh": "",      //案件编号
"bzr": "",       //比中人
"bzsjStart": "",      //开始比中时间
"bzsjEnd": "",       //结束比中时间
"lrsjStart": "",      //开始录入时间
"lrsjEnd": "",       //结束录入时间
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
"hitId": "",       //比中id
"ajbh": "",        //案件编号
"xczwbh": "",     //现场指纹编号
"szzwbh": "",     //十指指纹编号
"bzfs":"",        //比中方式
"bzr":"",         //比中人
"bzsj":"",        //比中时间
"lrsj":"",        //录入时间
"sjzt": ""       //数据状态
}
],
"pages": null,
"operates": null
}
````


### 指纹新增接口

#### API路径

```http
http://localhost:8081/ythpt/api/0/alims/handprint/add
```

后端格式为`/api/{recordLog}/api/0/alims/handprint/add`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
	"investigationId": "4028811b587603840158760384560000",//勘验id
	"handprintPhotoId": "4028811b587a4b0301587a4b03620000",//照片id
	"materialId": "4028811b5876038401587605a0c60015",//物证id
	"collectedBy": "4028811b5876038401587605a0c60015",//采集人id（技术人员id，页面展示跟现场信息录入的勘验人一样）
	"collectedByName": "李四",//（采集人姓名）
	"collectedDate": "2016-12-20",//采集日期
	"printCode": "20154541011",//
	collectionMode: "222"//采集方法（字典：ZWTQFFDM）
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
````


### 指纹修改接口

#### API路径

```http
http://localhost:8081/ythpt/api/0/alims/handprint/edit
```

后端格式为`/api/{recordLog}/api/0/alims/handprint/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
	"handprintPhotoId": "3028811b587a4b0301587a4b03620000",
	"collectedBy": "3028811b5876038401587605a0c60015",
	"collectedByName": "李呀",
	"collectedDate": "2017-12-20",
	"printCode": "10154541011",
	collectionMode: "224",
	"id": "4414CDCFC3497F1FE050A8C0C901181E"//手印id
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
````


### 指纹修改接口

#### API路径

```http
http://localhost:8081/ythpt/api/0/alims/handprint/delete
```

后端格式为`/api/{recordLog}/api/0/alims/handprint/delete`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
****
```json
"id": "4414CDCFC3497F1FE050A8C0C901181E"//手印id(不用jsonStr包裹)
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
````


### 指纹保存接口

#### API路径

```http
http://localhost:8081/ythpt/api/0/alims/handprint/save
```

后端格式为`/api/{recordLog}/api/0/alims/handprint/save`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
[{
	"investigationId": "4028811b587603840158760384560000",//勘验id
	"handprintPhotoId": "4028811b587a4b0301587a4b03620000",//照片id
	"materialId": "4028811b5876038401587605a0c60015",//物证id
	"collectedBy": "4028811b5876038401587605a0c60015",//采集人id（技术人员id，页面展示跟现场信息录入的勘验人一样）
	"collectedByName": "李四",//（采集人姓名）
	"collectedDate": "2016-12-20",//采集日期
	"printCode": "20154541011",//
	collectionMode: "222"//采集方法（字典：ZWTQFFDM）(无id表示新增)
},{
   "handprintPhotoId": "3028811b587a4b0301587a4b03620000",
   	"collectedBy": "3028811b5876038401587605a0c60015",
   	"collectedByName": "李呀",
   	"collectedDate": "2017-12-20",
   	"printCode": "10154541011",
   	collectionMode: "224",
   	"id": "4414CDCFC3497F1FE050A8C0C901181E"//手印id(有id表示修改)
}]
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
````

