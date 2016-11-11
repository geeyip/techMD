##DNA入库比对API文档

### 页面查询接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8080/api/0/alims/DNA/query
`````

后端格式为`/api/{recordLog}/alims/DNA/query`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "ajlx": "", //案件类型
  "faqh": "", //发案区划 字典代码
  "ybslsjBegin": "", //样本受理时间开始
  "ybslsjEnd": "", //样本受理时间结束
  "ajbh": "",  //案件编号
  "ajmc": "",  //案件名称
  "yblx": "",  //样本类型
  "jyzt": "", //检验状态
  "bbzt": "", //比对状态
  "jqbh": "", //警情编号
  "kybh": "", //勘验编号
  "fadd": "", //发案地点
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
			"id": "DC3BE807E29C43DFAE58B12A4EA93D3A",
			"xckyh": "J110145656985321322",
			"jqbh": "J110145656985321322",
			"ajbh": "A110145656985321323",
			"kysj": "2016-08-18",//Date类型
			"kydd": "朝阳XXX小区",
			"ajlb": "",
			"faqh": "",
			"fadd": "朝阳XXX小区",
			"kyr": "某某",
			"xczt":"",
			"sfyq": "2",//1:未逾期  2:已逾期
			"dxsl": 1, //短信条数
			"xxsl":2//消息条数
		}
    ],
    "pages": null,
    "operates": null
}
```
