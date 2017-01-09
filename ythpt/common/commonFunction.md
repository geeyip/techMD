## java后端方法调用API文档

### java后端方法调用接口

#### API路径

```java
1.API路径：http://localhost:8095/api/0/common_function/get_value
	后端格式为/api/{recordLog}/common_function/get_value，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	"className": "com.hisign.ythgzpt.util.NumberUtil",//类名
	"methodName": "numberArab2Cn",//方法名
	"para": ['200000901'], //参数
	"paraType": ['Integer'] //参数类型
4.返回值格式 {"flag":1,"totalCount":0,"msg":null,"data":"二亿零九百零一","pages":null,"operates":null}
```

### 获得java后端静态变量

#### API路径

```java
1.API路径：http://localhost:8095/api/0/common_function/get_filed
	后端格式为/api/{recordLog}/common_function/get_filed，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	"className": "com.hisign.ythgzpt.constant.Constants",//类名
	"fieldName": "USER_PASSWORD"//变量名
4.返回值格式 {"flag":1,"totalCount":0,"msg":null,"data":"hisign","pages":null,"operates":null}
```