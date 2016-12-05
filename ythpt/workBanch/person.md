## 人员管理API文档

### 勘验笔录制作查询接口

#### API路径

```http
http://localhost:8095/api/0/workbench/person/list
```

后端格式为`/api/{recordLog}/workbench/person/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{"pcdName":"SP_INT_API_SEL_PERSON_ALL", "pcdParamValMap":
{"pno":"aaa","birday":"2015-01-02", "idcard":"cc", "sex":"1","name":"tet","place":"350200000000",
"order":"1", "count":"200"}}
```

#### 返回值格式

```json

```
