## 勘验笔录检查API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8090/api/1/qualityCheck/kybl/list
```

后端格式为`/api/{recordLog}/qualityCheck/kybl/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**

```json
{
  "sfsc": "", //是否审查
  "sfhg": "", //是否合格
  "sfzg": "", //是否整改
  "investigationTimeStart": "",  //勘验开始时间
  "investigationTimeEnd": "",  //勘验结束时间
  "faqh": "",  //发案区划
  "investigationNo": "", //勘验编号
  "caseNo": "", //案件编号
  "jqbh": "", //警情编号
  "investigationPlace": "", //勘验地点
  "investigator": "", //勘验人
  "begin": 1,
  "end": 60
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
            'rownum': '1',
            'investigationId': '6E806CAB765A4051932A948F97BDC57A',
            'investigationNo': 'K1101126644646313233',
            'ajbh': 'A12312315451321211',
            'jqbh': 'J110145656985321324',
            'caseType': '入室盗窃',
            'faqh': 'xxx',
            'fadd': 'xxx',
            'investigationTime': '2015-01-0110: 00',
            'investigationPlace': '湖里校区110号',
            'investigator': '张三、李四',
            'lrr': '张三',
            'lrsj': '2015-01-0114: 00',
            'sfsc': '0',
            'sfhg': '1',
            'sfzg': '1',
            'tz': [
                1, //短信数
                2 //站内消息数量
            ],
            'fasj': '2016-08-1812: 25: 20',
            'kysy': 'xxx', //勘验事由
            'kyjcqk': 'xxx' //勘验检查情况
        }
    ],
    "pages": null,
    "operates": null
}
```

​	

### 审查页面 审查接口

进入修改页面后，保存修改时触发 

#### API 路径

```http
http://localhost:8090/api/1/qualityCheck/kybl/edit
```

后端格式为`/api/{recordLog}/qualityCheck/kybl/edit`,其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**

```json
{
    "investigationNo":"",//审查的勘验号
    "type": "1" //1：合格，0：不合格
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```