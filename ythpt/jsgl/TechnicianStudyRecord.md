##技术人员学习情况API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/technician/xxqk/list
```

后端格式为`/api/{recordLog}/jsgl/technician/xxqk/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": ""，             //技术人员id
"studyClass": "",          //培训班名称
"major": ""               //所属专业
"studyUnit": "",          //培训单位
"startTimeStart": ""      //培训时间开始
"endTimeEnd": ""          //培训时间终止
"hasBook": ""             //是否发证 0-否 1-是
"begin": 1,
"end": 200
}
```

#### 返回值格式

```json
{
"flag": 1,
"totalCount": 1,
"msg": null,
"data": [
{
"rownum": "1",
"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",       // 科研成果id
"techId": "",                                   // 技术人员id
"major",                                        // 所属专业
"studyUnit",                                    // 培训单位
"studyClass",                                   // 培训班名称
"startTimeStr",                                 // 培训开始时间
"endTimeStr",                                   // 培训结束时间
"studyTime",                                    // 培训时长
"hasBook",                                      // 是否发证 0-否 1-是
"bookPhotoId",                                  // 证书照片ID
}
],
"pages": null,
"operates": null
}
```
