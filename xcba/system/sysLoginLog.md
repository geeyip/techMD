# 系统登录日志API文档

* 页面查询接口（点击查询按钮时触发）

```java
1.API路径：http://localhost:8020/api/0/system/login/log
	后端格式为：api/{recordLog}/system/login/log（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr: {
        "oprUser": "sys",
        "logDateBegin": "2016-11-22",
        "logDateEnd": "2016-11-22",
        "begin": 1,
        "end": 200
    }
4.返回值格式：
  	{
        "flag": 1,
        "totalCount": 16,
        "msg": null,
        "data": [
            {
                "id": "80842CA6DF0F4982BC9C676037657922",
                "userName": null,
                "userPwd": null,
                "newPassword": null,
                "trueName": null,
                "openFlag": null,
                "openFlagZw": null,
                "policeId": null,
                "cardId": null,
                "userTel": null,
                "userUnit": null,
                "userUnitZh": null,
                "userLevel": null,
                "ipAddress": null,
                "createDate": "2016-11-22 15:27:18",
                "createPid": "sys",
                "defaultModule": null,
                "remark": null,
                "modifyDate": "2016-11-22 15:27:18",
                "modifyPid": "sys",
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
                "token": null,
                "logDateBegin": null,
                "logDateEnd": null,
                "oprUser": "sys",
                "oprUserName": "管理员",
                "oprUnit": "000000000000",
                "oprUnitCh": null,
                "logTime": "2016-11-22 15:27:18",
                "offTime": null,
                "createUnit": "000000000000",
                "ip": "192.168.1.120",
                "loginName": null,
                "rn": "1"
            },
            {
                .
                .
                .
            }
        ],
        "pages": null,
        "operates": null
    }
```