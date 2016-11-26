# 系统登录API文档

* 登录接口（点击登录按钮时触发）

```java
1.API路径：http://192.168.1.120:8020/xlcb/login
	后端格式为：/login
	前端调用:$post('http://192.168.1.120:8020/xlcb/login',{"username":"sys","password":"sys"},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "username":"sys",//用户账号
  	    "password":"sys"//用户密码
  	 }
4.返回值格式：
  	{
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data": {
            "rownum": null,
            "id": null,
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
            "pageLimit": null,
            "operateLimit": null,
            "token": "307fd2626f1c4c1cb9f137d68075cca3",
            "limits": {
                "operates": [],
                "pages": [
                    {
                        "rownum": null,
                        "id": null,
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
                        "moduleNo": "sys",
                        "parentId": null,
                        "title": "系统管理",
                        "description": "系统管理",
                        "openFlag": 1,
                        "createUser": null,
                        "createDatetime": "2006-07-01 17:04:01",
                        "updateUser": null,
                        "updateDatetime": "2016-11-21 17:04:27",
                        "rootId": null,
                        "moduleId": "ABCDEFGHABCDEFGHABCDEFGH22222209",
                        "permissionId": null,
                        "permisResId": null,
                        "resourceId": null,
                        "url": null,
                        "sort": "14",
                        "permissionDescription": "进入系统管理",
                        "resourceType": null,
                        "sysModulepermissionList": null,
                        "resources": [],
                        "modules": [],
                        "defaultInto": null,
                        "resourceStr": null,
                        "permissionFlag": 0,
                        "descriptionArray": null,
                        "resourceArray": null,
                        "name": null,
                        "resType": null,
                        "resString": null,
                        "operateNo": null,
                        "pageNo": "sys",
                        "items": [
                            {
                                "rownum": null,
                                "id": null,
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
                                "moduleNo": "sys",
                                "parentId": "ABCDEFGHABCDEFGHABCDEFGH22222209",
                                "title": "登录用户管理",
                                "description": "登录用户管理",
                                "openFlag": 1,
                                "createUser": null,
                                "createDatetime": "2015-11-27 10:04:01",
                                "updateUser": null,
                                "updateDatetime": "2016-06-16 14:24:12",
                                "rootId": null,
                                "moduleId": "ABCDEFGHABCDEFGHABCDEFGH22222208",
                                "permissionId": null,
                                "permisResId": null,
                                "resourceId": null,
                                "url": "sys-dlyhgl.html",
                                "sort": "1",
                                "permissionDescription": "进入登录用户管理",
                                "resourceType": null,
                                "sysModulepermissionList": null,
                                "resources": [],
                                "modules": [],
                                "defaultInto": null,
                                "resourceStr": null,
                                "permissionFlag": 0,
                                "descriptionArray": null,
                                "resourceArray": null,
                                "name": null,
                                "resType": null,
                                "resString": null,
                                "operateNo": null,
                                "pageNo": "sys-user-mng",
                                "items": null,
                                "sonMouleList": null
                            },
                            {
                                .
                                .
                                .
                            }
                        ],
                        "sonMouleList": null
                    }
                ]
            },
            "roles": [
                {
                    "cn": "市局用户",
                    "en": null
                },
                {
                    "cn": "超级管理员",
                    "en": "administrator"
                }
            ],
            "currentUser": {
                "id": "8af67d6247aa82060147aa8206c40000",
                "userName": "sys",
                "userPwd": "36bcbb801f5052739af8220c6ea51434",
                "newPassword": null,
                "trueName": "管理员",
                "openFlag": null,
                "openFlagZw": null,
                "policeId": null,
                "cardId": null,
                "userTel": null,
                "userUnit": null,
                "userUnitZh": null,
                "userLevel": null,
                "ipAddress": "192.168.1.120",
                "createDate": null,
                "createPid": null,
                "defaultModule": null,
                "remark": null,
                "modifyDate": null,
                "modifyPid": null,
                "rownum": null,
                "sysUserRoleIds": null,
                "begin": 0,
                "end": 0,
                "roleId": null,
                "roleName": null,
                "roleNameString": null,
                "sortName": null,
                "sortOrder": null,
                "orderByString": null,
                "token": null
            },
            "clientKey": "HjVhY003qberNQ%2Frpavq43qTnO0RWwQqg4FMvPPRXENj8kSiYtjOiE1InKh2VwazuO5fPMrbOKen%0D%0
                            AXr44U4KnNrTLohhODacgR%2FwvF9jpKdiZ63G7FcvIErFnbAl6h8HK9VMd9M%2FdiNXPBPU5iOlxNuc
                            h%0D%0ATLNKNCpa%2F8WD7aZ8re0%3D",
            "sysParam": {
                        "dataInterface": "http://192.168.1.151:8080/datacenter/api/apiService?token=pubservice",
                        "deploy_place": "滨州市公安局刑事技术一体化平台",
                        "caseLinkAddress": null,
                        "personLinkAddress": null,
                        "system-version": "V1.0.0"
                    }
        },
        "pages": null,
        "operates": null
    }
```


* 注销接口（点击注销按钮时触发）

```java
1.API路径：http://192.168.1.120:8020/xlcb/logout
	后端格式为：/logout
	前端调用:$post('http://192.168.1.120:8020/xlcb/logout',{"username":"sys","password":"sys"},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "username":"sys"//用户账号
  	 }
4.返回值格式：
    {
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data": null,
        "pages": null,
        "operates": null
    }
```

* 小类考核通报列表接口（进入登录页时获取数据时触发）

```java
1.API路径：http://192.168.1.120:8020/xlcb/sys/xlkh/list
	后端格式为：/sys/xlkh/list
	前端调用：$post('http://192.168.1.120:8020/xlcb/sys/xlkh/list',null,o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
  	无传入参数
4.返回值格式：
    {
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data": [
            "2016-10-20",
            "2016-11-20",
            "2016-09-20"
        ],
        "pages": null,
        "operates": null
    }
```


* 小类考核通报查询接口（点击标注数据时(window.open方式)触发）

```java
1.API路径：http://192.168.1.120:8020/xlcb/sys/xlkh/view
	后端格式为：/sys/xlkh/view
	前端调用:window.open(http://192.168.1.120:8020/xlcb/sys/xlkh/view?tagDate=2016-09)
2.请求：POST, application/json
3.传入参数格式：
  	tagDate:"2016-09"
4.返回值格式：
    无返回值
```


* 首页趋势图数据接口（进入首页时触发）

```java
1.API路径：http://192.168.1.120:8020/xlcb/sys/xlkh/viewChart
	后端格式为：/sys/xlkh/viewChart
	前段调用:$post('http://192.168.1.120:8020/xlcb/sys/xlkh/viewChart',{pcdName:"SP_TAG_API_SEL_CASE_TREND"},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
           pcdName:"SP_TAG_API_SEL_CASE_TREND"
     }
4.返回值格式：
    {
            "flag": 1,
            "totalCount": 2,//平均值
            "msg": null,
            "data":
                [
                    {
                        "time": "11月",//时间
                        "casenum":"20"//案件数
                    },
                    {
                        "time": "10月",//时间
                        "casenum":"25"//案件数
                    }
                ],
            "pages": null,
            "operates": null
        }
```







