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



