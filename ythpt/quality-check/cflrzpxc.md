# 重复录入照片现场检查API文档

* 页面查询接口（点击查询按钮时触发）

```java
1.API路径：http://localhost:8090/api/1/qualityCheck/cflrzpxc/list
    后端格式为：/api/{recordLog}/qualityCheck/cflrzpxc/list（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr: {
	    "sfrd": "", //是否认定-add
	    "rdyj": "", //认定意见-add
	    "sfzg": "", //是否整改-add
	    "investigationTimeStart": "",  //勘验开始时间
	    "investigationTimeEnd": "",  //勘验结束时间
	    "faqh": "",  //发案区划-add
	    "investigationNo": "", //勘验编号
	    "caseNo": "", //案件编号
	    "jqbh": "", //警情编号-add
	    "investigationPlace": "", //勘验地点
	    "caseType": "", //案件类别
	    "begin": 1,
	    "end": 60
	}
4.返回值格式：
  	{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data": [
		{
			"rownum": "1",
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"sfrd": "0",
			"sfzg": "0",
			"xckyInfo": [
				{
					"rownum": "1",
					"investigationId": "A93F2F10874F4A7CB25FC6D261B26B6E",
					"investigationNo": "K4403070305002010092684",
					"investigationTime": "2016-08-11 12:12:25",
					"investigator": "张三、李四",
					"investigationPlace": "月华小区",
					"kyUnit": "Unit",
					"kyCheckSit": "7月6日13时0分接到东华在北京在2016年7月6日13时0分接到东华在北京市房山区发生一起入户抢劫案。",
					"caseNo": "A4401066000002013120101",
					"jqbh": "J370700447005201005000004",
					"caseType": "入室盗窃案",
					"faqh": "湖里派出所",
					"lrdw": "录入单位",
					"picInfo": [
						{"id":"", "base64":""}
					],  //重复照片
					"rdSuggest": "未认定",
					"sfzg": "0"
				}
			]
		}
    ],
    "pages": null,
    "operates": null
}
```



* 页面修改保存接口（进入修改页面后，保存修改时触发 ）

```java
1.API路径：http://localhost:8090/api/1/qualityCheck/cflrzpxc/edit
	后端格式为：/api/{recordLog}/qualityCheck/cflrzpxc/edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：  (list的值为认定为重复现场或者非重复现场的勘验id)
jsonStr: {
    "type": "1",  //1:认定为重复现场 0:认定为非重复现场
    "list": [
        "A93F2F10874F4A7CB25FC6D261B26B67",
        "A93F2F10874F4A7CB25FC6D261B26B68"
    ]
}
4.返回值格式：
  	{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

