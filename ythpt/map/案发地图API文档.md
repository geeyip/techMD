## 案发地图API文档

### 条件查询接口

表单中输入区划，时间，性质等条件，点击查询按钮时触发

#### API路径

```http
http://localhost:8090/api/1/system/casemap/searchform
```

后端格式为`/api/{recordLog}/system/casemap/searchform`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{ "ajxz":958, "faqh":1023, "fasj":“2016-08-31,2016-09-02”}
```

#### 返回值格式

```json
{"flag":1,"totalCount":2,"data":[
		{
		"ajmc":"达斡小区盗窃案",     //发案名称
		"fadz":'光明街11号',	      //发案地址
		"fasj":"2016-02-13 14:32",//发案时间
		"kybh":"K9998762345",     //勘验编号
		"ajxz":"盗窃案", //案件性质（类别）	   "zasd":0,  		 //作案手段   	"lng":112.2356, //经度   	"lat":69.365,	 //纬度   	},
   	{
		"ajmc":"广浩小区盗窃案",
		"fadz":'光明街25号',
		"fasj":"2016-06-22 15:16",
		"kybh":"K9998762321",
		"ajxz":"盗窃案",	   "zasd":0,   	"lng":130.8532,   	"lat":72.068,   	}
	]
}
```

### 绘制区域查询接口

鼠标拖拽区域，拖拽完成时触发

#### API路径

```http
http://localhost:8090/api/1/system/casemap/searchdraw
```

后端格式为`/api/{recordLog}/system/casemap/searchdraw`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json {ul:{lng:117.5439,lat:65.492}, Ll:{lng:117.869,lat:64.173},ajxz:007 }
```

#### 返回值格式

```json
{"flag":1,"totalCount":2,"data":[
		{
		"ajmc":"达斡小区盗窃案",     //发案名称
		"fadz":'光明街11号',	      //发案地址
		"fasj":"2016-02-13 14:32",//发案时间
		"kybh":"K9998762345",     //勘验编号
		"ajxz":"盗窃案", //案件性质（类别）	   "zasd":0,  		 //作案手段   	"lng":112.2356, //经度   	"lat":69.365,	 //纬度   	},
   	{
		"ajmc":"广浩小区盗窃案",
		"fadz":'光明街25号',
		"fasj":"2016-06-22 15:16",
		"kybh":"K9998762321",
		"ajxz":"盗窃案",	   "zasd":0,   	"lng":130.8532,   	"lat":72.068,   	}
	]
}
```

### 半径范围查询接口

选中地图某点和相关半径，点击查询按钮时触发

#### API路径

```http
http://localhost:8090/api/1/system/casemap/searchradius
```

后端格式为`/api/{recordLog}/system/casemap/searchradius`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{ point:{lng:117.5439,lat:65.492}, radius:1000，ajxz:007} )
```

#### 返回值格式

```json
{"flag":1,"totalCount":2,"data":[
		{
		"ajmc":"达斡小区盗窃案",     //发案名称
		"fadz":'光明街11号',	      //发案地址
		"fasj":"2016-02-13 14:32",//发案时间
		"kybh":"K9998762345",     //勘验编号
		"ajxz":"盗窃案", //案件性质（类别）	   "zasd":0,  		 //作案手段   	"lng":112.2356, //经度   	"lat":69.365,	 //纬度   	},
   	{
		"ajmc":"广浩小区盗窃案",
		"fadz":'光明街25号',
		"fasj":"2016-06-22 15:16",
		"kybh":"K9998762321",
		"ajxz":"盗窃案",	   "zasd":0,   	"lng":130.8532,   	"lat":72.068,   	}
	]
}
```

