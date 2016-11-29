## 字典管理API文档

###查询列表接口

#### API路径

```http
http://localhost:8095/api/0/system/dict_mng/list
```

后端格式为`/api/{recordLog}/system/dict_mng/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{
"dictValue":"类别代码","dictKey":"","openFlag":"1","py":"JklB","root":"JKLB",
"parentKey":"",//默认parentKey，进入根节点的下级节点后使用
"defaultRoot":""//默认root_key，进入根节点后使用
}
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null,"data":
[{"rownum":"1","id":"5377B9AF711142DE84EC29965F37E69K","user":null,"del":null,"secrecy":null,"createDate":null
,"modifyDate":null,"transferTime":null,"rev1":null,"rev2":null,"rev3":null,"rev4":null,"rev5":null,"rev6":null,
"rev7":null,"rev8":null,"begin":0,"end":0,"sortOrder":null,"sortName":null,"orderByString":null,"key":"JKLBDM",
"value":"监控类别代码","parentKey":null,"localId":null,"root":"JKLBDM","keys":null,"queryString":null,
"queryType":null,"py":"JKLB","openFlag":"有效","defaultRoot":null,"remark":null,
"sort":0,"isParent":"1","dictKey":"JKLBDM","dictValue":"监控类别代码"}],"pages":null,"operates":null}
```