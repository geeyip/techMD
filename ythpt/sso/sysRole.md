## 系统角色管理API文档

###查询列表接口

#### API路径

```http
http://localhost:8095/api/0/system/role/list_sso
```

后端格式为`/api/{recordLog}/system/role/list_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{
"begin":1,"end":3,"sortName":"createTime","sortOrder":"desc",
"queryCondition":{"roleName":"管理员","superId":"1","note":""}
}
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null,"data":
[{"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,
"lastSys":null,"roleId":"151e19acae5744caa1b33e92598af53d","roleName":"系统管理员","superId":"1","type":0,"note":null}],
"pages":null,"operates":null}
```

###角色新增接口

#### API路径

```http
http://localhost:8095/api/0/system/role/add_sso
```

后端格式为`/api/{recordLog}/system/role/add_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{"roleName":"测试人员","superId":"1","note":"测试人员","type":"1"}
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":"146cee1b01894228b8527904f2ff8d2b","pages":null,"operates":null}
```

###角色修改接口

#### API路径

```http
http://localhost:8095/api/0/system/role/update_sso
```

后端格式为`/api/{recordLog}/system/role/update_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{"roleName":"测试人员test","superId":"0","note":"测试人员test","type":"2","roleId":"146cee1b01894228b8527904f2ff8d2b"}
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

###进入角色授权接口

#### API路径

```http
http://localhost:8095/api/0/system/role/_permission_sso
```

后端格式为`/api/{recordLog}/system/role/_permission_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```
systemId:"ALIMS",
roleId:"11c1c54720e04024b641f25fd843c81c",
startId:"acd57f855ab44ce3a183852300124f25"
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":{"allMenus":
[{"systemId":"ALIMS","resourceId":"d3afe865a4954dfea7145503aee7147b","resourceName":"123213",
"resourceEnName":"12321313","superId":"5ff8a4700e5942fb86cb85b0fce0a28f","name":"123213",
"url":null,"state":null,"icon":null,"visibleState":0,"orderNum":0,"note":null,"menuType":1,"children":null}],
"menuType":0,"systemId":"ALIMS","authedMenus":
[{"systemId":"ALIMS","resourceId":"f1fc77a98af544698b167013aec2d29a","resourceName":"个人待办事项一览",
"resourceEnName":"test","superId":"2643dd360b6443938a3dce5ae09006e9","name":"个人待办事项一览",
":1,"orderNum":1,"note":"teste","menuType":0,"children":null}],
"roleId":"11c1c54720e04024b641f25fd843c81c"},
"superMenus":
[{"systemId":"ALIMS","resourceId":"f1fc77a98af544698b167013aec2d29a","resourceName":"个人待办事项一览",
"resourceEnName":"test","superId":"2643dd360b6443938a3dce5ae09006e9","name":"个人待办事项一览",
":1,"orderNum":1,"note":"teste","menuType":0,"children":null}],
"roleId":"11c1c54720e04024b641f25fd843c81c"},
"currentMenus":
[{"systemId":"ALIMS","resourceId":"f1fc77a98af544698b167013aec2d29a","resourceName":"个人待办事项一览",
"resourceEnName":"test","superId":"2643dd360b6443938a3dce5ae09006e9","name":"个人待办事项一览",
":1,"orderNum":1,"note":"teste","menuType":0,"children":null}],
"roleId":"11c1c54720e04024b641f25fd843c81c"},
"pages":null,"operates":null}
```

###角色授权接口

#### API路径

```http
http://localhost:8095/api/0/system/role/permission_sso
```

后端格式为`/api/{recordLog}/system/role/permission_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{
"resourceId":"5ff8a4700e5942fb86cb85b0fce0a28f,acd57f855ab44ce3a183852300124f25",
"roleId":"146cee1b01894228b8527904f2ff8d2b",
"systemId":"YTH"
}
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":"","data":null,"pages":null,"operates":null}
```

###进入用户分配接口

#### API路径

```http
http://localhost:8095/api/0/system/role/_user_sso
```

后端格式为`/api/{recordLog}/system/role/_user_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
roleId:146cee1b01894228b8527904f2ff8d2b
systemid:XCKY
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":
{ "token":"862d39f7ffed4b2888fa48728d8e5398","roleId":null,"systemid":"XCKY",
"noRoleId":"146cee1b01894228b8527904f2ff8d2b","checkUsers":[],
"uncheckUsers":[{"status":0,"createAccount":null,"createTime":0,"lastModifyTime":0,"lastModifyAccount":null,
"lastTerminal":null,"lastSys":null,"indexNum":0,"userId":"e3c88eaaffd74d0582bbe480e208d75e",
"userName":"1","sex":0,"cid":"123456789009876","isPolice":0,"policeId":"1","contact":"1",
"avatar":null,"post":null,"postName":null,"birth":0,"poli":null,"poliName":null,
"phone":null,"fax":null,"address":null,"zipcode":null,"province":null,"provinceName":null,
"city":null,"cityName":null,"county":null,"countyName":null,"extStr1":null,"extStr2":null,"extStr3":null,
"account":"1","pass":"C4CA4238A0B923820DCC509A6F75849B","userType":0,"activeStatus":1,
"orgId":"e6f8da5304e0420e8935f54e271b7e82","orgName":"南安市公安局刑侦大队四中队","orgCode":"350583240500",
"orgType":1,"roleName":null}]},
"pages":null,"operates":null}
```


###根据id获得角色数据接口

#### API路径

```http
http://localhost:8095/api/0/system/role/view_sso
```

后端格式为`/api/{recordLog}/system/role/view_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```
roleId:a450de5ff27e454f90d2cc5f9c178b93
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":
{"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,
"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"a450de5ff27e454f90d2cc5f9c178b93","roleName":"中心最高管理者",
"superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},"pages":null,"operates":null}
```

###根据id删除角色

#### API路径

```http
http://localhost:8095/api/0/system/role/delete_sso
```

后端格式为`/api/{recordLog}/system/role/delete_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
roleId:a450de5ff27e454f90d2cc5f9c178b93
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

###角色加入用户

#### API路径

```http
http://localhost:8095/api/0/system/role/add_user_sso
```

后端格式为`/api/{recordLog}/system/role/add_user_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
roleId:a450de5ff27e454f90d2cc5f9c178b93
checkUsers:124125,452158
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

###角色移除用户

#### API路径

```http
http://localhost:8095/api/0/system/role/remove_user_sso
```

后端格式为`/api/{recordLog}/system/role/remove_user_sso，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
roleId:a450de5ff27e454f90d2cc5f9c178b93
unCheckUsers:124125,452158
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```