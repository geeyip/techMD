## 盗抢骗现场检查API文档

### 一、页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8090/api/1/qualityCheck/dqp/list
```

后端格式为`/api/{recordLog}/qualityCheck/dqp/list`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**

```json
{
  "znjc":"",  //智能检查规则  1：满足，0：不满足
  "sfrd":"", //是否认定 1：已认定 0：未认定
  "sfzg":"",//是否整改 1：已整改，0：未整改
  "investigationTimeStart": "",//勘验开始时间
  "investigationTimeEnd": "",//勘验结束时间
  "faqh": "",//发案区划
  "snw":"",//室内外
  "ajlb":"",//案件类别
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
          'investigationId': 'A93F2F10874F4A7CB25FC6D261B26B6E',
          'investigationNo': 'K4403070305002010092684',
          'caseNo': 'A4401066000002013120101',
          'caseType': '入室盗窃案',
          'faqh': 'xxx',
          'fadd': 'xxx',
          'investigationTime': '2016-08-1112: 25: 20',
          'investigationPlace': 'xxx',
          'investigator': '张三、李四',
          'znjc': '1', //1：满足，0：不满足
          'sfrd': '0',//是否认定
          'score': '3',//分值
          'snw': '0',//室内、室外
          'xq': 'xxx',//详情
          'sfzg': '1',//是否整改
          'tz': [
              1,
              2
          ]
      }
  ],
    "pages": null,
    "operates": null
}
```

### 二、进入质量检查、进入查看 

点击审查按钮时触发

#### API路径

```http
http://localhost:8090/api/1/qualityCheck/dqp/edit
```

后端格式为`/api/{recordLog}/qualityCheck/dqp/edit`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式

**jsonStr:**

```json
{
  "investigationNo":""//勘验编号
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
          'proDesc': '现场方位图', 
          'proPics': [
            {"base64":""}//缩略图的base64编码
          ],  //现场图 没有图片数组为空
          'proDesc': 'xxxx',//现场描述
          'jcnr': '名称、指北、制作单位、人、时间等要素是否齐全。', //检查内容
          'value': 1,//分值
          'checkRes': '1',//是否满意 1：是，0-否 （进入查看是必须要）
          'score': '0'//得分（进入查看是必须要）
      }
	],
    "pages": null,
    "operates": null
}
```

### 三、质量检查 合格、不合格

点击查看按钮时触发

#### API路径

```http
http://localhost:8090/api/1/qualityCheck/dqp/check
```

后端格式为`/api/{recordLog}/qualityCheck/dqp/check`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式

**jsonStr:**

```json
{
    "type": "1",  //1：合格，0：不合格
    "investigationNo": "K4403070305002010092684" //现勘编号
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```