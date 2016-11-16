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
"PageNum":1,"PageSize":5,"orderBy":"createTime","sort":"desc","queryCondition":
{"roleName":"系统管理员","superId":"1","note":""}
}
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null,"data":
[{"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,
"lastSys":null,"roleId":"151e19acae5744caa1b33e92598af53d","roleName":"系统管理员","superId":"1","type":0,"note":null}],
"pages":null,"operates":null}
```