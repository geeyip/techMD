##技术人员论文著作情况API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/api/1/jsgl/technician/lwzzqk/list
```

后端格式为`/api/{recordLog}/jsgl/technician/lwzzqk/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"techId": ""，              //技术人员id
"paperTitle": "",          //论文、著作标题
"publishName": ""          //刊物名称
"publishUnit": "",         //刊物(论文交流)主办单位
"publishDateStart": ""     //发布时间开始
"publishDateEnd": ""       //发布时间结束
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
"paperTitle",                                   // 论文著作标题
"paperAuthor",                                  // 作者
"publishName",                                  // 刊物名称
"publishDateStr",                               // 发布出版时间
"publishRank",                                  // 排名
"publishNo",                                    // 刊号
"publishUnit",                                  // 刊物(论文交流)主办单位
}
],
"pages": null,
"operates": null
}
```
