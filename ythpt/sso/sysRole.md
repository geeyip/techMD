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
systemId:"XCKY",
account:"900504"
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":{
"allMenus":
[{"systemId":"XCKY","resourceId":"1EB4B74996094FEA9CA221F408BB9B5B","resourceName":"现场信息录入","superId":"7D3B3CBBE4374CB39A9892AAB43D4D21","name":"现场信息录入","url":"sceneCollecting/xcky-xcxxlr.html","state":"sceneCollecting/xcky-xcxxlr.html","icon":null,"visibleState":0,"orderNum":1,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"EBCDEFGHABCDEFGHABCDEFGH22222201","resourceName":"首页","superId":null,"name":"首页","url":"fst-page.html","state":"fst-page.html","icon":null,"visibleState":0,"orderNum":1,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"ABCDEFGHABCDEFGHABCDEFGH22222208","resourceName":"登录用户管理","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"登录用户管理","url":"system/sys-dlyhgl.html","state":"system/sys-dlyhgl.html","icon":null,"visibleState":0,"orderNum":1,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"7D3B3CBBE4374CB39A9892AAB43D4D21","resourceName":"现场勘验","superId":null,"name":"现场勘验","url":null,"state":null,"icon":null,"visibleState":0,"orderNum":2,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"D7ACEF7B5F664CA3B8940342039F58E1","resourceName":"案件勘验","superId":"7D3B3CBBE4374CB39A9892AAB43D4D21","name":"案件勘验","url":"sceneCollecting/xcky-ajky.html","state":"sceneCollecting/xcky-ajky.html","icon":null,"visibleState":0,"orderNum":2,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"ABCDEFGHABCDEFGHABCDEFGH22222207","resourceName":"系统角色管理","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"系统角色管理","url":"system/sys-xtjsgl.html","state":"system/sys-xtjsgl.html","icon":null,"visibleState":0,"orderNum":2,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"D1BDEFGHABCDEFGHABCDEFGA22222201","resourceName":"系统参数管理","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"系统参数管理","url":"system/sys-xtcsgl.html","state":"system/sys-xtcsgl.html","icon":null,"visibleState":0,"orderNum":3,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"ABCDEFGHABCDEFGHABCDEFGH22222209","resourceName":"系统管理","superId":null,"name":"系统管理","url":null,"state":null,"icon":null,"visibleState":0,"orderNum":3,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"3EDC3A43BB21420CA404853F6E7D0B74","resourceName":"系统模块管理","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"系统模块管理","url":"system/sys-xtmkgl.html","state":"system/sys-xtmkgl.html","icon":null,"visibleState":0,"orderNum":4,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"9D2D4A5BEB7843B699C2176E945F23D3","resourceName":"系统登录日志","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"系统登录日志","url":"system/sys-loginlog.html","state":"system/sys-loginlog.html","icon":null,"visibleState":0,"orderNum":5,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"0757F585692449019CF791EFA3021F02","resourceName":"系统导航","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"系统导航","url":"system/sys-xtdh.html","state":"system/sys-xtdh.html","icon":null,"visibleState":0,"orderNum":6,"note":null,"menuType":0,"children":null}
],
"account":"900504","systemId":"XCKY","authedMenus":
[{"systemId":"XCKY","resourceId":"1EB4B74996094FEA9CA221F408BB9B5B","resourceName":"现场信息录入","superId":"7D3B3CBBE4374CB39A9892AAB43D4D21","name":"现场信息录入","url":"sceneCollecting/xcky-xcxxlr.html","state":"sceneCollecting/xcky-xcxxlr.html","icon":null,"visibleState":0,"orderNum":1,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"EBCDEFGHABCDEFGHABCDEFGH22222201","resourceName":"首页","superId":null,"name":"首页","url":"fst-page.html","state":"fst-page.html","icon":null,"visibleState":0,"orderNum":1,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"ABCDEFGHABCDEFGHABCDEFGH22222208","resourceName":"登录用户管理","superId":"ABCDEFGHABCDEFGHABCDEFGH22222209","name":"登录用户管理","url":"system/sys-dlyhgl.html","state":"system/sys-dlyhgl.html","icon":null,"visibleState":0,"orderNum":1,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"7D3B3CBBE4374CB39A9892AAB43D4D21","resourceName":"现场勘验","superId":null,"name":"现场勘验","url":null,"state":null,"icon":null,"visibleState":0,"orderNum":2,"note":null,"menuType":0,"children":null},
{"systemId":"XCKY","resourceId":"D7ACEF7B5F664CA3B8940342039F58E1","resourceName":"案件勘验","superId":"7D3B3CBBE4374CB39A9892AAB43D4D21","name":"案件勘验","url":"sceneCollecting/xcky-ajky.html","state":"sceneCollecting/xcky-ajky.html","icon":null,"visibleState":0,"orderNum":2,"note":null,"menuType":0,"children":null}
]
},"pages":null,"operates":null}
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