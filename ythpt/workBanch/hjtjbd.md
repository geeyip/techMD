## 痕迹提交比对API文档

###痕迹数量接口

#### API路径

```http
http://localhost:8095/api/0/workbench/hjtjbd/hj_count
```

后端格式为`/api/{recordLog}/workbench/hjtjbd/hj_count`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```
无传入参数
```

#### 返回值格式
```json
{
"flag":1,"totalCount":1,"msg":null,
"data":{"xchj_zj":0,"dtjhj_ywc":0,"xchj_dna":0,"wtjhj_ywc":0,"wtjhj_wwc":0,"dtjhj_wwc":0,"xchj_zw":0},
"pages":null,"operates":null
}
```