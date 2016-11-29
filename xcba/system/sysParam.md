# 系统参数管理API文档

* 页面查询接口（进入系统参数列表页）

```java
1.API路径：http://localhost:8020/pi/0/system/param
	后端格式为：api/{recordLog}/system/param（其中{recordLog}为前端传入，
                标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	无传入参数
4.返回值格式：
    {
        "flag": 1,
        "totalCount": 2,
        "msg": null,
        "data": [
            {
                "rownum": "1",
                "id": "629AD78EE04340519A841F2D3A08F851",
                "user": null,
                "del": "0",
                "secrecy": null,
                "createDate": null,
                "modifyDate": null,
                "transferTime": null,
                "rev1": null,
                "rev2": null,
                "rev3": null,
                "rev4": null,
                "rev5": null,
                "rev6": null,
                "rev7": null,
                "rev8": null,
                "begin": 0,
                "end": 0,
                "sortOrder": null,
                "sortName": null,
                "orderByString": null,
                "key": null,
                "value": null,
                "parentKey": null,
                "localId": null,
                "seq": "1",
                "chineseName": "系统配置",
                "englishName": "xtpz",
                "createUser": "sys",
                "createDatetime": "2016-04-01 15:15:29",
                "updateUser": null,
                "updateDatetime": null,
                "sysParamList": [
                    {
                        "rownum": "1",
                        "id": "A8A41F2B148340559BF75A623BEFDA67",
                        "user": null,
                        "del": null,
                        "secrecy": null,
                        "createDate": null,
                        "modifyDate": null,
                        "transferTime": null,
                        "rev1": null,
                        "rev2": null,
                        "rev3": null,
                        "rev4": null,
                        "rev5": null,
                        "rev6": null,
                        "rev7": null,
                        "rev8": null,
                        "begin": 0,
                        "end": 0,
                        "sortOrder": null,
                        "sortName": null,
                        "orderByString": null,
                        "key": null,
                        "value": "滨州市公安局刑事技术一体化平台",
                        "parentKey": null,
                        "localId": null,
                        "chineseName": "系统名称设置",
                        "englishName": "deploy_place",
                        "defaultValue": null,
                        "createUser": "sys",
                        "createDatetime": "2016-08-30 15:00:57",
                        "updateUser": null,
                        "updateDatetime": "2016-11-19 14:45:50",
                        "remark": null,
                        "option": null,
                        "paramType": "0",
                        "dictType": null,
                        "configId": "629AD78EE04340519A841F2D3A08F851",
                        "hideFlag": "0",
                        "paramSort": "1",
                        "deleteFlag": null,
                        "name": null,
                        "paramEditId": null
                    },
                    {
                        .
                        .
                        .
                    }
                ]
            },
            {
                "rownum": "2",
                "id": "52A7ACF920AD4E4694EEFC77286EE222",
                "user": null,
                "del": "0",
                "secrecy": null,
                "createDate": null,
                "modifyDate": null,
                "transferTime": null,
                "rev1": null,
                "rev2": null,
                "rev3": null,
                "rev4": null,
                "rev5": null,
                "rev6": null,
                "rev7": null,
                "rev8": null,
                "begin": 0,
                "end": 0,
                "sortOrder": null,
                "sortName": null,
                "orderByString": null,
                "key": null,
                "value": null,
                "parentKey": null,
                "localId": null,
                "seq": "2",
                "chineseName": "链接地址",
                "englishName": "ljdz",
                "createUser": "sys",
                "createDatetime": "2016-04-01 15:15:29",
                "updateUser": null,
                "updateDatetime": null,
                "sysParamList": [
                    {
                        "rownum": "2",
                        "id": "7A193039CFDA423B96C34F4577F59245",
                        "user": null,
                        "del": null,
                        "secrecy": null,
                        "createDate": null,
                        "modifyDate": null,
                        "transferTime": null,
                        "rev1": null,
                        "rev2": null,
                        "rev3": null,
                        "rev4": null,
                        "rev5": null,
                        "rev6": null,
                        "rev7": null,
                        "rev8": null,
                        "begin": 0,
                        "end": 0,
                        "sortOrder": null,
                        "sortName": null,
                        "orderByString": null,
                        "key": null,
                        "value": null,
                        "parentKey": null,
                        "localId": null,
                        "chineseName": "案件链接地址",
                        "englishName": "caseLinkAddress",
                        "defaultValue": null,
                        "createUser": "sys",
                        "createDatetime": "2016-11-19 14:43:45",
                        "updateUser": null,
                        "updateDatetime": "2016-11-19 14:44:27",
                        "remark": null,
                        "option": null,
                        "paramType": "1",
                        "dictType": null,
                        "configId": "52A7ACF920AD4E4694EEFC77286EE222",
                        "hideFlag": "0",
                        "paramSort": "1",
                        "deleteFlag": null,
                        "name": null,
                        "paramEditId": null
                    },
                    {
                        .
                        .
                        .
                    }
                ]
            }
        ],
        "pages": null,
        "operates": null
    }
```


* 页面新增接口（点击新增按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/param/add
	后端格式为：/xlcb/api/{recordLog}/system/param/add（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "chineseName":"test",//参数中文名
  	    "englishName":"test",//参数英文名
        "value":"test",//参数值
        "defaultValue":"test",//参数默认值
        "hideFlag":"0",//是否隐藏(字典选择)
        "paramSort":"4",//页面排序
        "paramType":"0",//参数类型(字典选择:CSLXDM)
        "configId":"629AD78EE04340519A841F2D3A08F851",//所属模块
        "remark":"dadsadad"//备注
  	 }
4.返回值格式：
    {
    "flag": 1,
    "totalCount": 0,
    "msg": "success",
    "data": null,
    "pages": null,
    "operates": null
    }
```


* 页面更新接口（点击保存按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/param/edit
	后端格式为：/xlcb/api/{recordLog}/system/param/edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{
        [
            {
                "name": "deploy_place",
                "value": "滨州市公安局刑事技术一体化平台"
            },
            {
                "name": "system-version",
                "value": "V1.0.0"
            },
            {
                "name": "test",
                "value": "1111"
            },
            {
                "name": "qqq",
                "value": "qqqaa"
            }
        ]
    }
4.返回值格式：
    {
        "flag": 1,
        "totalCount": 0,
        "msg": "success",
        "data": null,
        "pages": null,
        "operates": null
    }
 ```


* 页面修改接口（点击参数名时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/param/update
后端格式为：/xlcb/api/{recordLog}/system/param/update（其中{recordLog}为前端传入，
  标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{
        "englishName": "qqq111",
        "paramSort": "5",
        "chineseName": "qqqqwww11",
        "remark": "ewqeqe",
        "value": "qqqaa112",
        "paramEditId": "31AA744AB97C4F09B4505C6F65BA617D",
        "defaultValue": "qqq",
        "hideFlag": "0",
        "dictType": "1",
        "paramType": "1",
        "configId": "629AD78EE04340519A841F2D3A08F851"
     }
4.返回值格式：
    {
    "flag": 1,
    "totalCount": 0,
    "msg": "success",
    "data": null,
    "pages": null,
    "operates": null
    }
```








