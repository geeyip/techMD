# 系统用户管理API文档

* 页面查询接口（点击查询按钮时触发）

```java
1.API路径：http://localhost:8090/api/1/system/user/list
	后端格式为：/api/{recordLog}/system/user/list（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{"userName":"test","trueName":"","roleName":"test","begin":1,"end":60}
4.返回值格式：
  	{
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data": [
        {
            "id": "5c20d013cbf2439dbbdb346e5b88b392",
            "userName": "test",
            "userPwd": "98f6bcd4621d373cade4e832627b4f6",
            "userPwd2": null,
            "newPassword": null,
            "roleNameString": " test",
            "policeId": null,
            "cardId": null,
            "userTel": null,
            "userUnitZh": null,
            "notContainUserName": null,
            "userLevel": "1",
            "defaultModule": "0",
            "ipFlag": null,
            "ipAddress": null,
            "remark": null,
            "deleteFlag": null,
            "transferTime": null,
            "createUnit": null,
            "createUnitCn": null,
            "createDate": null,
            "createUserId": null,
            "createUser": "管理员",
            "modifyUser": null,
            "createUserName": null,
            "modifyDate": null,
            "modifyUserId": null,
            "modifyUserName": null,
            "createDatetime": "2016-08-02 15:10:15",
            "modifyDatetime": null,
            "rownum": "1",
            "sysUserRoleIds": null,
            "rev1": null,
            "rev2": null,
            "rev3": null,
            "rev4": null,
            "rev5": null,
            "rev6": null,
            "rev7": null,
            "rev8": null,
            "openFlag": "1",
            "openFlagZw": "有效",
            "trueName": "test",
            "userUnit": null,
            "begin": 0,
            "end": 0,
            "roleId": null,
            "roleName": null,
            "sortName": null,
            "sortOrder": null,
            "orderByString": null,
            "token": null
        }
    ],
    "pages": null,
    "operates": null
}
```



* 页面修改保存接口（进入修改页面后，保存修改时触发）

```java
1.API路径：http://localhost:8090/api/1/system/user/edit
	后端格式为：/api/{recordLog}/system/user/edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:
	{
          "remark": "",
          "userTel": "",
          "openFlag": "1",
          "newPassword": "",
          "trueName": "test",
          "userName": "test",
          "sysUserRoleIds": "c783054387a24e38ad7a7a92a8bbee54",
          "userId": "5c20d013cbf2439dbbdb346e5b88b392"
      }
4.返回值格式：
  	{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

