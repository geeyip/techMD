##技术人员科研成果API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/technician/kycg/list
```

后端格式为`/api/{recordLog}/jsgl/technician/kycg/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": ""，             //技术人员id
"startTimeStart": "",     //开始时间起始
"startTimeEnd": ""        //开始时间终止
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
"startTimeStr": "",                             // 开始时间
"endTimeStr": "",                               // 结束时间
"workDetail": "",                               // 完成情况
"workRole":"",                                  // 本人作用
"workResult":"",                                // 完成效果
"workFileId":""                                 // 附件id
}
],
"pages": null,
"operates": null
}
```
