# 系统用户管理API文档

* 页面查询接口（点击查询按钮时触发）

```java
1.API路径：http://localhost:8020/api/1/system/user/list
	后端格式为：/api/{recordLog}/system/user/list（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "userName":"test",//用户账户
  	    "trueName":"test",//用户姓名
  	    "roleName":"test",//角色字符串(输入中文)
  	    "userUnit":"440000000000",//用户单位代码
  	    "openFlag":"1",//是否启用(输入代码:1:有效,0:无效)
  	    "begin":1,
  	    "end":60
  	 }
4.返回值格式：
  	{
    "flag":1,
    "totalCount":7705,
    "msg":null,
    "data": [
        {
            "id":"3cf39cb57d26416c9191a2fec9507024",//ID
            "userName":"testtest",//用户账号
            "userPwd":null,//用户密码
            "newPassword":null,//新密码
            "trueName":"滕剑",//用户姓名
            "openFlag":"1",//账号状态
            "openFlagZw":"有效",//账号状态中文
            "policeId":null,//警号ID
            "cardId":null,//身份证号
            "userTel":null,//用户电话
            "userUnit":null,//用户单位代码
            "userUnitZh":null,//用户单位中文
            "userLevel":"1",//用户级别
            "ipAddress":null,//IP地址
            "createDate":"2016-10-13 09:40:49",
            "createPid":"sys",//创建人账号
            "defaultModule":null,//默认模块
            "remark":null,//备注
            "modifyDate":"2016-10-20 11:33:01",
            "modifyPid":null,//修改人账号
            "rownum":"1",//序号
            "sysUserRoleIds":null,
            "begin":0,
            "end":0,
            "roleId":null,
            "roleName":null,
            "roleNameString":null,//用户角色字符串
            "sortName":null,//排序字段名
            "sortOrder":null,//排序规则
            "orderByString":null,//排序字符串
            "token":null
        }
    ],
    "pages":null,
    "operates":null
}
```


* 页面新增接口（点击保存按钮时触发）

```java
1.API路径：http://localhost:8020/api/1/system/user/add
	后端格式为：/api/{recordLog}/system/user/add（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
  	jsonStr:{
  	    "userName":"test",//用户账户
  	    "trueName":"test",//用户姓名
  	    "userPwd":"123456",//用户密码
  	    "openFlag":"1",//用户账户是否有效(传入代码)
  	    "userUnit":"440000000000",//用户单位代码
  	    "policeId":"1234567",//用户警号
        "cardId":"400162199111201271",//身份证号
        "userTel":"18368894577",//电话号码
        "remark":"test"//备注
  	 }
4.返回值格式：
  	{
    "flag":1,
    "totalCount":0,
    "msg":null,
    "data":"e22e527ac68846529451bf1f433a47d8",//ID
    "pages":null,
    "operates":null
}
```


* 页面进入修改接口（点击列表修改按钮时触发）

```java
1.API路径：http://localhost:8020/api/0/system/user/_edit
	后端格式为：/api/{recordLog}/system/user/_edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：GET, application/json
3.传入参数格式：
  	jsonStr:{
  	    "id":"test"//ID
  	 }
4.返回值格式：
  	{
  	"flag":1,
  	"totalCount":1,
  	"msg":null,
  	"data":{
  	    "roleList":[
  	        {
  	            "rownum":"2",
  	            "id":"d8069828d7944a0db078501a0db73842",
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
  	            "roleName":"分县局用户",
  	            "description":"查看所有、标注本分县局侵财",
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
  	    ]
  	    "sysUser":
  	    {
  	        "id":"e22e527ac68846529451bf1f433a47d8",
  	        "userName":"aaa",
  	        "userPwd":null,
  	        "newPassword":null,
  	        "trueName":"adsa",
  	        "openFlag":"1",
  	        "openFlagZw":"启用",
  	        "policeId":"213132",
  	        "cardId":null,
  	        "userTel":null,
  	        "userUnit":"321312312312",
  	        "userUnitZh":null,
  	        "userLevel":"1",
  	        "ipAddress":null,
  	        "createDate":"2016-11-22 09:46:32",
  	        "createPid":"sys",
  	        "defaultModule":null,
  	        "remark":null,
  	        "modifyDate":"2016-11-22 09:46:32",
  	        "modifyPid":null,
  	        "rownum":null,
  	        "sysUserRoleIds":null,
  	        "begin":0,
  	        "end":0,
  	        "roleId":null,
  	        "roleName":null,
  	        "roleNameString":null,
  	        "sortName":null,
  	        "sortOrder":null,
  	        "orderByString":null,
  	        "token":null
  	     },
  	     "sysUserRoleIds":""
  	},
  	"pages":null,
  	"operates":null
    }
```


* 页面修改接口（点击修改按钮时触发）

```java
1.API路径：http://localhost:8020/api/1/system/user/edit
	后端格式为：/api/{recordLog}/system/user/edit（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{
            "userName":"test",//用户账户
            "trueName":"test",//用户姓名
            "newPassword":"123456",//用户新密码
            "openFlag":"1",//用户账户是否有效(传入代码)
            "userUnit":"440000000000",//用户单位代码
            "policeId":"1234567",//用户警号
            "cardId":"400162199111201271",//身份证号
            "userTel":"18368894577",//电话号码
            "remark":"test",//备注
            "sysUserRoleIds":"68034b57bbf74c31bf962b14d87909db,d8069828d7944a0db078501a0db73842"//角色字符串
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

* 页面查看接口（点击列表用户账号时触发）

```java
1.API路径：http://localhost:8020/api/0/system/user/view
	后端格式为：/api/{recordLog}/system/user/view（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：GET, application/json
3.传入参数格式：
    jsonStr:{
      	    "id":"test"//ID
    }
4.返回值格式：
    {
    "flag":1,
    "totalCount":0,
    "msg":null,
    "data":
        {
        "id":"e22e527ac68846529451bf1f433a47d8",
        "userName":"aaa",
        "userPwd":null,
        "newPassword":null,
        "trueName":"23113",
        "openFlag":"1",
        "openFlagZw":"启用",
        "policeId":"321312",
        "cardId":null,
        "userTel":null,
        "userUnit":"1111",
        "userUnitZh":null,
        "userLevel":"1",
        "ipAddress":null,
        "createDate":"2016-11-22 09:46:32",
        "createPid":"sys",
        "defaultModule":null,
        "remark":null,
        "modifyDate":"2016-11-22 10:10:46",
        "modifyPid":"sys",
        "rownum":null,
        "sysUserRoleIds":null,
        "begin":0,
        "end":0,
        "roleId":null,
        "roleName":null,
        "roleNameString":" 派出所用户、分县局用户",
        "sortName":null,
        "sortOrder":null,
        "orderByString":null,
        "token":null
        },
    "pages":null,
    "operates":null
    }
```

* 页面删除接口（点击列表删除按钮时触发）

```java
1.API路径：http://localhost:8020/api/0/system/user/view
	后端格式为：/api/{recordLog}/system/user/view（其中{recordLog}为前端传入，
      标识是否需要记录操作日志）
2.请求：POST, application/json
3.传入参数格式：
    jsonStr:{
      	    "id":"test"//ID
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