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
"value":"案件类型代码","key":"","openFlag":"1","py":"ajlx","root":"AJLBDM",
"parentKey":"",//默认parentKey，进入根节点的下级节点后使用
"defaultRoot":""//默认root_key，进入根节点后使用
}
```

#### 返回值格式
```json

```