# 系统模块管理API文档

* 页面查询接口（初始进入模块）

```java
1.API路径：http://localhost:8080/api/0/system/module
	后端格式为：api/{recordLog}/system/module（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	无参数
4.返回值格式：
  	{
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data": [
            {
                "systemId": "YTHPT",
                "resourceId": "5ff8a4700e5942fb86cb85b0fce0a28f",
                "resourceName": "首页",
                "superId": null,
                "children":null,
                "icon":null,
                "menuType":0,
                "name":"首页",
                "note":"首页",
                "orderNum":1,
                "resourceId":"5ff8a4700e5942fb86cb85b0fce0a28f",
                "resourceName":"首页",
                "state":"www.baidu.com",
                "superId":null,
                "systemId":"ALIMS",
                "url":"www.baidu.com",
                "visibleState":1
            },
            {
                .
                .
                .
            }
        ],
        "flag":1,
        "msg":null,
        "operates":null,
        "pages":null,
        "totalCount":0
    }
```


* 页面模块查看接口（查看模块信息）

```java
1.API路径：http://localhost:8080/api/0/system/view
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
                "systemId": "YTHPT",
                "resourceId": "5ff8a4700e5942fb86cb85b0fce0a28f",
                "resourceName": "首页",
                "superId": null,
                "children":null,
                "icon":null,
                "menuType":0,
                "name":"首页",
                "note":"首页",
                "orderNum":1,
                "resourceId":"5ff8a4700e5942fb86cb85b0fce0a28f",
                "resourceName":"首页",
                "state":"www.baidu.com",
                "superId":null,
                "systemId":"ALIMS",
                "url":"www.baidu.com",
                "visibleState":1
            }
        ],
        flag:1
        "msg":"success"
        "operates":null
        "pages":null
        "totalCount":0
    }
```


* 页面模块添加接口（添加模块）

```java
1.API路径：http://localhost:8080/api/1/system/add
	后端格式为：api/{recordLog}/system/add（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
        "resourceId":"",
        "rootId":"",
        "permisResId":"",
        "permissionId":"",
        "parentId":"4148ebf55e784a7a9306d72b2ad18af5",
        "defaultInto":"",
        "url":"1",
        "sort":"1",
        "moduleNo":"11",
        "description":"22",
        "openFlag":"1",
        "title":"111"
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
1.API路径：http://localhost:8080/api/1/system/update
	后端格式为：api/{recordLog}/system/update（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{
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
1.API路径：http://localhost:8020/api/1/system/delete
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
