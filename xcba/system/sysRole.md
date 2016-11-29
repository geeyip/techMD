# 系统角色管理API文档

* 页面查询接口（点击查询按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/list
	后端格式为：/xlcb/api/{recordLog}/system/role/list（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "roleName":"派出所",//角色名
  	    "description":"本所侵财",//角色描述
  	    "begin":1,
  	    "end":200
  	 }
4.返回值格式：
  	{
  	"flag":1,
  	"totalCount":1,
  	"msg":null,
  	"data":
  	    [
  	        {
  	        "rownum":"1",
  	        "id":"68034b57bbf74c31bf962b14d87909db",
  	        "user":null,
  	        "del":null,
  	        "secrecy":null,
  	        "createDate":null,
  	        "modifyDate":null,
  	        "transferTime":null,
  	        "rev1":null,
  	        "rev2":null
  	        ,"rev3":null,
  	        "rev4":null,
  	        "rev5":null,
  	        "rev6":null,
  	        "rev7":null,
  	        "rev8":null,
  	        "begin":0,
  	        "end":0,
  	        "sortOrder":null,
  	        "sortName":null,
  	        "orderByString":null,
  	        "key":null,
  	        "value":null,
  	        "parentKey":null,
  	        "localId":null,
  	        "users":null,
  	        "roleId":null,
  	        "permissions":null,
  	        "roleName":"派出所用户",
  	        "description":"查看所有、标注本所侵财",
  	        "openFlag":"1",
  	        "openFlagZw":"启用",
  	        "roleNameEn":null,
  	        "a":null
  	        },
  	        {
  	            .
  	            .
  	            .
  	        }
  	    ],
  	"pages":null,
  	"operates":null
  }
```


* 页面新增接口（点击新增按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/add
	后端格式为：/xlcb/api/{recordLog}/system/role/add（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "roleName":"派出所",//角色名
  	    "description":"本所侵财",//角色描述
  	    "openFlag":"1"//角色是否启用.1:启用,0:禁用
  	 }
4.返回值格式：
    {
    "flag":1,
    "totalCount":0,
    "msg":null,
    "data":null,
    "pages":null,
    "operates":null
    }
```



* 页面删除接口（点击列表删除按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/delete
	后端格式为：/xlcb/api/{recordLog}/system/role/delete（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"93cc7ba5b5dc41118dffc1d2eb668812"//ID
  	 }
4.返回值格式：
    {
    "flag":1,
    "totalCount":0,
    "msg":null,
    "data":null,
    "pages":null,
    "operates":null
    }
```


* 页面进入修改接口（点击列表修改按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/0/system/role/_edit
	后端格式为：/xlcb/api/{recordLog}/system/role/_edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：GET, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"93cc7ba5b5dc41118dffc1d2eb668812"//ID
  	 }
4.返回值格式：
    {
    "flag":1,
    "totalCount":0,
    "msg":null,
    "data":
        {
        "rownum":"1",
        "id":"2e3c3e9d134f4ec3bb2bc83d07dba73d",
        "user":null,
        "del":null,
        "secrecy":null,
        "createDate":null,
        "modifyDate":null,
        "transferTime":null,
        "rev1":null,
        "rev2":null,
        "rev3":null,
        "rev4":null,
        "rev5":null,
        "rev6":null,
        "rev7":null,
        "rev8":null,
        "begin":0,
        "end":0,
        "sortOrder":null,
        "sortName":null,
        "orderByString":null,
        "key":null,
        "value":null,
        "parentKey":null,
        "localId":null,
        "users":null,
        "roleId":null,
        "permissions":null,
        "roleName":"超级超级管理员",
        "description":"哈哈哈哈哈哈",
        "openFlag":"1",
        "openFlagZw":"启用",
        "roleNameEn":null,
        "a":null
         },
    "pages":null,
    "operates":null
}
```


* 页面修改接口（点击修改按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/edit
	后端格式为：/xlcb/api/{recordLog}/system/role/edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "roleName":"派出所",//角色名
        "description":"本所侵财",//角色描述
        "openFlag":"1"//角色是否启用.1:启用,0:禁用
  	 }
4.返回值格式：
    {
    "flag":1,
    "totalCount":0,
    "msg":null,
    "data":null,
    "pages":null,
    "operates":null
    }
```


* 页面选择权限接口（点击列表选择权限按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/0/system/role/_permission
	后端格式为：/xlcb/api/{recordLog}/system/role/_permission（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：GET, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"2e3c3e9d134f4ec3bb2bc83d07dba73d",//ID
  	    "moduleId":"ABCDEFGHABCDEFGHABCDEFGH22222209"//模块ID
  	 }
4.返回值格式：
{
    "flag": 1,
    "totalCount": 0,
    "msg": null,
    "data": {
        "moduleList": [
            {
                "rownum": null,
                "id": "D1BDEFGHABCDEFGHABCDEFGA22222201",
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
                "title": "系统参数管理",
                "description": "系统参数管理",
                "openFlag": 1,
                "createUser": null,
                "createDatetime": null,
                "updateUser": null,
                "updateDatetime": null,
                "rootId": null,
                "moduleId": null,
                "permissionId": null,
                "permisResId": null,
                "resourceId": null,
                "url": null,
                "sort": null,
                "permissionDescription": null,
                "resourceType": null,
                "sysModulepermissionList": [
                    {
                        "rownum": null,
                        "id": "HBCDEFGHJFCDEFGHABCDEFGH52346040",
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
                        "moduleId": "D1BDEFGHABCDEFGHABCDEFGA22222201",
                        "name": "HBCDEFGHJFCDEFGHABCDEFGH52346040",
                        "operation": null,
                        "description": "进入系统参数管理",
                        "openFlag": "1",
                        "permissionFlag": null
                    }
                ],
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
                "pageNo": null,
                "items": null,
                "sonMouleList": []
            },
            {
                .
                .
                .
            }
        ],
        "sysRolePermisList": [],
        "sysModuleList": [
            {
                "rownum": null,
                "id": "ABCDEFGHABCDEFGHABCDEFGH22222209",
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
                "openFlag": 0,
                "createUser": null,
                "createDatetime": null,
                "updateUser": null,
                "updateDatetime": null,
                "rootId": null,
                "moduleId": null,
                "permissionId": null,
                "permisResId": null,
                "resourceId": null,
                "url": null,
                "sort": null,
                "permissionDescription": null,
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
                "pageNo": null,
                "items": null,
                "sonMouleList": null
            }
        ],
        "permission": [
            {
                "rownum": null,
                "id": "ABCDEFGHABCDEFGHABCDEFGH12346047",
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
                "moduleId": "ABCDEFGHABCDEFGHABCDEFGH22222209",
                "name": "ABCDEFGHABCDEFGHABCDEFGH12346047",
                "operation": null,
                "description": "进入系统管理",
                "openFlag": "1",
                "permissionFlag": null
            }
        ],
        "sysRole": {
            "rownum": "1",
            "id": "2e3c3e9d134f4ec3bb2bc83d07dba73d",
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
            "users": null,
            "roleId": null,
            "permissions": null,
            "roleName": "超级超级管理员",
            "description": "哈哈哈哈哈哈1",
            "openFlag": "1",
            "openFlagZw": "启用",
            "roleNameEn": null,
            "a": null
        }
    },
    "pages": null,
    "operates": null
}
```


* 页面权限接口（点击授权按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/permission
	后端格式为：/xlcb/api/{recordLog}/system/role/permission（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：GET, application/json
3.传入参数格式：
  	jsonStr:{
  	    "roleId":"2e3c3e9d134f4ec3bb2bc83d07dba73d",//角色ID
  	    "sysRolePermisIds":"ABCDEFGHABCDEFGHABCDEFGH12346047,HBCDEFGHJFCDEFGHABCDEFGH52346040",//角色选中的对应权限值
  	    "currentRolePermisIds":"
  	        ABCDEFGHABCDEFGHABCDEFGH12346047,HBCDEFGHJFCDEFGHABCDEFGH52346040,
  	        EF23D49BD20B49A2BF5CDDC8297CE151,B218F256A70242DE91C2C6C68C64D131
  	        ,ABCDEFGHABCDEFGHABCDEFGH12346048,ABCDEFGHABCDEFGHABCDEFGH12346049"//所有开启的模块权限
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


* 页面角色分配用户接口（点击列表分配用户按钮时触发）

```java
1.API路径：http://localhost:8020/xlcb/api/0/system/role/_user
	后端格式为：/xlcb/api/{recordLog}/system/role/_user（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：GET, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"2e3c3e9d134f4ec3bb2bc83d07dba73d"//角色ID
  	 }
4.返回值格式：
    {
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data": {
            "associatedUserList": [],
            "allUserList": [
                {
                    "id": "3f1eecb0e8f6458694f140972a76ac7f",
                    "userName": "gao111",
                    "userPwd": null,
                    "newPassword": null,
                    "trueName": "gao333",
                    "openFlag": "1",
                    "openFlagZw": "启用",
                    "policeId": "963258",
                    "cardId": "52",
                    "userTel": "66",
                    "userUnit": "3300000000",
                    "userUnitZh": null,
                    "userLevel": "1",
                    "ipAddress": null,
                    "createDate": "2016-11-21 15:42:27",
                    "createPid": "sys",
                    "defaultModule": null,
                    "remark": "fwrrew41243qd",
                    "modifyDate": "2016-11-21 17:37:21",
                    "modifyPid": "gao111",
                    "rownum": "1",
                    "sysUserRoleIds": null,
                    "begin": 0,
                    "end": 0,
                    "roleId": null,
                    "roleName": null,
                    "roleNameString": " 派出所用户",
                    "sortName": null,
                    "sortOrder": null,
                    "orderByString": null,
                    "token": null
                },
                {
                    .
                    .
                    .
                }
            ],
            "sysRole": {
                "rownum": "1",
                "id": "2e3c3e9d134f4ec3bb2bc83d07dba73d",
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
                "users": null,
                "roleId": null,
                "permissions": null,
                "roleName": "超级超级管理员",
                "description": "哈哈哈哈哈哈1",
                "openFlag": "1",
                "openFlagZw": "启用",
                "roleNameEn": null,
                "a": null
            }
        },
        "pages": null,
        "operates": null
    }
```


* 页面角色加入用户接口（角色分配用户页面触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/add_user
	后端格式为：/xlcb/api/{recordLog}/system/role/add_user（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"2e3c3e9d134f4ec3bb2bc83d07dba73d",//ID
  	    "selectUserId":"3f1eecb0e8f6458694f140972a76ac7f,8af67d6247aa82060147aa8206c40000"//选择的用户
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


* 页面角色移除用户接口（角色分配用户页面触发）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/role/remove_user
	后端格式为：/xlcb/api/{recordLog}/system/role/remove_user（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"2e3c3e9d134f4ec3bb2bc83d07dba73d",//ID
  	    "associatedUserId":"3f1eecb0e8f6458694f140972a76ac7f,8af67d6247aa82060147aa8206c40000"//选择的用户
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









