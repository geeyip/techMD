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


###字典新增接口

#### API路径

```http
http://localhost:8095/api/0/system/dict_mng/add
```

后端格式为`/api/{recordLog}/system/dict_mng/add，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{"dictLevel":"0","dictValue":"查询类别代码","dictKey":"CXLBDM","openFlag":"1",
"py":"CXLBDM","root":"CXLBDM","sort":"1","leafFlag":"0","remark":"233","parentKey":""}
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

###字典修改接口

#### API路径

```http
http://localhost:8095/api/0/system/dict_mng/edit
```

后端格式为`/api/{recordLog}/system/dict_mng/edit，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{"id":"b5d4cba6767346a8b6c63578f2bf5b42","dictValue":"警情查询11","dictKey":"111","openFlag":"1",
"py":"AJ","sort":"3","remark":"235",root:"CXLBDM",parentKey:"11"}
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

###字典删除接口

#### API路径

```http
http://localhost:8095/api/0/system/dict_mng/delete
```

后端格式为`/api/{recordLog}/system/dict_mng/delete，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{"id":"3db0f3190ce049d6803b233c074a61ae"}
```

#### 返回值格式
```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```

###获取单个字典接口

#### API路径

```http
http://localhost:8095/api/0/system/dict_mng/dict_info
```

后端格式为`/api/{recordLog}/system/dict_mng/dict_info，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
jsonStr:
{"id":"1cb90ba884d74e468b3efc0b727d9b22"}
```

#### 返回值格式
```json
{"flag":1,"totalCount":1,"msg":null,"data":{"rownum":null,"id":"1cb90ba884d74e468b3efc0b727d9b22",
"user":null,"del":null,"secrecy":null,"createDate":null,"modifyDate":null,"transferTime":null,"rev1":null,
"rev2":null,"rev3":null,"rev4":null,"rev5":null,"rev6":null,"rev7":null,"rev8":null,"begin":0,"end":0,
"sortOrder":null,"sortName":null,"orderByString":null,"key":"12","value":"警情查询","parentKey":"CXLBDM",
"localId":null,"root":"CXLBDM","keys":null,"queryString":null,"queryType":null,"py":"AJCXDM","openFlag":"0",
"defaultRoot":null,"remark":"234","sort":2,"isParent":null,"dictLevel":"0","leafFlag":null,"dictKey":"12",
"dictValue":"警情查询"},"pages":null,"operates":null}
```

###字典导出接口

#### API路径

```http
http://localhost:8095/api/0/system/dict_mng/export
```

后端格式为`/api/{recordLog}/system/dict_mng/export，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
```
无传入参数
```

#### 返回值格式
```json
无返回参数
```