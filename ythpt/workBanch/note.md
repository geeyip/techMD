## 勘验笔录制作API文档

### 勘验笔录制作查询接口

#### API路径

```http
http://localhost:8095/api/0/workbench/kyblzz/list
```

后端格式为`/api/{recordLog}/workbench/kyblzz/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
	"begin": 1,
	"end": 60,
	"faqh": "350200000000",
	"ajlb": "050101",
	"kysjStart": "2016-06-23",
	"kysjEnd": "2016-06-25",
	"investigationNo": "K3502062",
	"kydd": "厦门市",
	"fadd": "湖里区",
	"investigatorId": "8a023cd43a8b154e013ad89786032b67",
	"sfzz": "1"
}
```

#### 返回值格式

```json
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"dqpSatisfyFlag": null,
		"fwsytAmount": 0,
		"pmsytAmount": 0,
		"fwzpAmount": 0,
		"gmzpAmount": 0,
		"zdbwzpAmount": 0,
		"casePlace": null,
		"investigationId": "8a023cd4554c85f701559643f0285a59",
		"investigationNo": "K3502062400002016060208",
		"investigator": null,
		"investigatorId": "8a023cd43a8b154e013ad89786032b67,8a023cd43a8b154e013ad89785f42b61",
		"investigationPlace": null,
		"qualifiedFlag": "已提交",
		"saveFlag": null,
		"finishFlag": null,
		"investigationTime": null,
		"isToCase": null,
		"lawId": null,
		"exposureProcess": null,
		"director": null,
		"content": null,
		"updatedInvestNoteId": "8a023cd4559650470155965f46ba015a",
		"fileName": "k4441234.doc",
		"kybh": null,
		"jqbh": null,
		"ajbh": "A3502062400002016060159",
		"kysj": "2016-06-23 17:00",
		"kydd": "福建省厦门市湖里区林后社63号百佳批发部",
		"ajlb": "入户抢劫案",
		"faqh": null,
		"fadd": "福建省厦门市湖里区林后社63号百佳批发部",
		"kyr": "王恩宽、王书龙",
		"xczt": null,
		"sfyq": null,
		"dxsl": 0,
		"xxsl": 0,
		"sfgl": null,
		"zdjkajl": null,
		"kysjStart": null,
		"kysjEnd": null,
		"kysjDate": "2016-06-23 17:00:00",
		"bhglx": null,
		"jcxx": 0
	}],
	"pages": null,
	"operates": null
}
```
