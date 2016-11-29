# 系统模块管理API文档

* 页面查询接口（初始进入模块）

```java
1.API路径：http://localhost:8020/xlcb/api/0/system/module
	后端格式为：api/{recordLog}/system/module（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	无参数
4.返回值格式：
  	{
        "flag": 1,
        "totalCount": 6,
        "msg": null,
        "data": [
            {
                "rownum": null,
                "id": "ABCDEFGHABCDEFGHABCDEFGH22222208",
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
                "createUser": "test",
                "createDatetime": "2015-11-27 10:04:01",
                "updateUser": "sys",
                "updateDatetime": "2016-06-16 14:24:12",
                "rootId": "ABCDEFGHABCDEFGHABCDEFGH22222209",
                "moduleId": null,
                "permissionId": null,
                "permisResId": null,
                "resourceId": null,
                "url": "sys-dlyhgl.html",
                "sort": "1",
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


* 页面模块查看接口（查看模块信息）

```java
1.API路径：http://localhost:8020/xlcb/api/0/system/view
	后端格式为：api/{recordLog}/system/view（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{"moduleId":"ABCDEFGHABCDEFGHABCDEFGH22222209"}
4.返回值格式：
    {
        "flag": 1,
        "totalCount": 0,
        "msg": "success",
        "data": [
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
                "rootId": "ABCDEFGHABCDEFGHABCDEFGH22222209",
                "moduleId": "ABCDEFGHABCDEFGHABCDEFGH22222209",
                "permissionId": "ABCDEFGHABCDEFGHABCDEFGH12346047",
                "permisResId": "ABCDEFGHABCDEFGHABCDEFGH12346265",
                "resourceId": "ABCDEFGHABCDEFGHABCDEFGH12346156",
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
                "operateNo": "sys",
                "pageNo": null,
                "items": null,
                "sonMouleList": null
            }
        ],
        "pages": null,
        "operates": null
    }
```


* 页面模块添加接口（添加模块）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/add
	后端格式为：api/{recordLog}/system/add（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr: {
        "resourceId": "",
        "rootId": "",
        "permisResId": "",
        "permissionId": "",
        "parentId": "",
        "defaultInto": "",
        "url": "",
        "sort": "2",
        "resourceStr": "dasda",
        "moduleNo": "dasda",
        "description": "dada",
        "openFlag": "1",
        "title": "dads"
    }
4.返回值格式：
    {
    "flag": 1,
    "totalCount": 0,
    "msg": "保存成功",
    "data": null,
    "pages": null,
    "operates": null
    }
```


* 页面模块修改接口（修改模块）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/update
	后端格式为：api/{recordLog}/system/update（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{
    "resourceStr": "www",
    "sort": "2",
    "rootId": "39918EB2B5904A1ABA9B827F0D58270D",
    "url": "",
    "parentId": "39918EB2B5904A1ABA9B827F0D58270D",
    "title": "www",
    "resourceId": "53CFADB3196D430CBEB5A036CF56DB79",
    "moduleNo": "dasda",
    "description": "www",
    "defaultInto": "",
    "permisResId": "A00C729B901441CA94966EEC75D5E209",
    "permissionId": "E840D8C76C99430A9759B9EC773EB5BF",
    "openFlag": "1"
    }
4.返回值格式：
    {
    "flag": 1,
    "totalCount": 0,
    "msg": "保存成功",
    "data": null,
    "pages": null,
    "operates": null
    }
```


* 页面模块删除接口（删除模块）

```java
1.API路径：http://localhost:8020/xlcb/api/1/system/delete
	后端格式为：api/{recordLog}/system/delete（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{"moduleId":"39918EB2B5904A1ABA9B827F0D58270D"}
4.返回值格式：
    {
    "flag": 1,
    "totalCount": 0,
    "msg": "删除成功",
    "data": null,
    "pages": null,
    "operates": null
    }
```
