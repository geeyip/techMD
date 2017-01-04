## 系统参数管理API文档

* 参数查询接口（点击参数管理时触发）

```java
1.API路径：http://localhost:8090/api/0/system/param
	后端格式为/api/{recordLog}/system/param，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{}
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "id": "629AD78EE04340519A841F2D3A08F851",
                "seq": "1",
                "chineseName": "系统配置",
                "englishName": "xtpz",
                "del": "0",
                "createUser": null,
                "createDatetime": null,
                "updateUser": null,
                "updateDatetime": null,
                "sysParamList": [{
                	"configId":"629AD78EE04340519A841F2D3A08F851",
                	"id":"402881f30d2e65bb010d2e6684360831",
                	"chineseName": "短消息刷新时间间隔",
                 	"englishName": "MSG_READ_INTERVAL",
                 	"value": "50000",
                 	"defaultValue": null,
                 	"remark": "毫秒",
                 	"paramType": "0",
                 	"dictType": null,
                 	"hideFlag": "0",
                 	"paramSort": null,
                 	"createUser": null,
                 	"createDatetime": null,
                 	"updateUser": null,
                 	"updateDatetime": null
    			}]
            }
        ],
        "pages": null,
        "operates": null
    }
```



- 参数新增接口（点击弹出新增页面，点击保存按钮时触发）

```java
1.API路径：http://localhost:8090/api/1/system/add
	后端格式为/api/{recordLog}/system/add，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:
	{
  		"chineseName":"短消息刷新时间间隔",
  		"englishName":"MSG_READ_INTERVAL",
  		"value":"50000",
  		"defaultValue":null,
  		"hideFlag":"0",
  		"paramSort":null,
  		"paramType":"0",
  		"configId":"629AD78EE04340519A841F2D3A08F851",
  		"dictType":null,
  		"remark":"毫秒"
	}
4.返回值格式	{"flag":1,"totalCount":null,"msg":"success","data":null,"pages":null,"operates":null}
```



- 参数修改接口（点击保存时触发）

```java
1.API路径：http://localhost:8090/api/1/system/edit
	后端格式为/api/{recordLog}/system/edit，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:
	[{
  		"name":"MSG_READ_INTERVAL",
  		"value":"50000"
	},{
  		"name":"popMessage",
  		"value":"8"
	}]
4.返回值格式	{"flag":1,"totalCount":null,"msg":"success","data":null,"pages":null,"operates":null}
```

- 盗抢骗规则保存（点击保存时触发）
```java
1.API路径：http://localhost:8090/api/0/system/param/dqp/save_rule
	后端格式为/api/{recordLog}/system/param/dqp/save_rule，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:
[{
	"ruleKey": "xctAmount",
	"ruleKeyDesc": "现场图",
	"ruleValue": "1",
	"comparator": "1",//比较符，字典代码：BJDM
	"ruleValueDesc": "张"
}]
4.返回值格式	{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

- 盗抢骗规则查询（进入页面时触发）
```java
1.API路径：http://localhost:8090/api/0/system/param/dqp/get_rule
	后端格式为/api/{recordLog}/system/param/dqp/get_rule，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：GET, application/json
3.传入参数格式：无传入参数
4.返回值格式
{
	"flag": 1,
	"totalCount": 0,
	"msg": null,
	"data": [{
		"id": "44DD46A7A9FD90CBE050A8C0C9010EA7",
		"monitorType": "0205",
		"ruleKey": "xctAmount",
		"ruleKeyDesc": "现场图",
		"ruleValue": "1",
		"ruleValueDesc": "张",
		"comparator": "1",
		"deleteFlag": null,
		"createUser": null,
		"createDateTime": null,
		"updateUser": null,
		"updateDateTime": null,
		"overDays": null,
		"startTime": null,
		"isIncludePreData": null,
		"caseTypeName": null,
		"ajlbDict": null,
		"isAutoSendMsg": null,
		"isDefaultSelectEd": null,
		"isBgData": null,
		"isJdData": null,
		"evidenceType": null,
		"personIdArr": null,
		"organIdArr": null,
		"user": null
	}],
	"pages": null,
	"operates": null
}
```


- 数字转换
```java
1.API路径：http://localhost:8090/api/0/system/param/number
	后端格式为/api/{recordLog}/system/param/number，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
jsonStr:['2', '23354', '20', '1435354333']
type : 1  //转换类型(1-阿拉伯转汉字，2-汉字转阿拉伯，3-阿拉伯转汉字（汉字含特殊习惯用语）)
4.返回值格式
{"flag":1,"totalCount":0,"msg":null,
"data":["二","二万三千三百五十四","二十","一十四亿三千五百三十五万四千三百三十三"],
"pages":null,"operates":null
}
```