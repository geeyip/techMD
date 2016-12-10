## 违法人员信息采集API文档

### 违法人员信息采集查询接口

#### API路径

```http
http://localhost:8095/api/0/illegalperson/collect/list
```

后端格式为`/api/{recordLog}/illegalperson/collect/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
$post('http://localhost:8090/api/0/illegalperson/collect/list', {
	"pcdName": "SP_INT_API_SEL_CRI_PERSON",
	"pcdParamValMap": {
		pno: '',
		hno: '',
		name: '',
		sex: '',
		idcard: '',
		place: '',
		unit: '',
		status: '',
		collflag: '',
		birdaymi: '',
		birdayma: ''
	},
	"begin": "1",
	"end": "5"
},
function(res) {
	log(res)
},
true)
```

#### 返回值格式

```json
{
	"flag": 1,
	"totalCount": 1000,
	"msg": null,
	"data": [{
		"unit": "厦门市公安局巡逻特警支队巡警湖里大队二中队",
		"num": 1,
		"sex": "1",
		"collflag": "0",
		"birday": "1989-11-22 00:00:00",
		"status": "未抓获",
		"name": "杨通刚",
		"idcard": "522624197906082612",
		"hno": null,
		"house": "贵州省三穗县良上乡上寨村土地塘组",
		"pno": "R3506272305002009100007"
	},
	{
		"unit": null,
		"num": 2,
		"sex": "1",
		"collflag": "0",
		"birday": "1988-03-15 00:00:00",
		"status": "未抓获",
		"name": "陈志",
		"idcard": "35012819880315431X",
		"hno": null,
		"house": "厦门市思明区体育路61号",
		"pno": "0000000207120000603379"
	},
	{
		"unit": null,
		"num": 3,
		"sex": "1",
		"collflag": "0",
		"birday": "1990-11-15 00:00:00",
		"status": "未抓获",
		"name": "柏孟林",
		"idcard": "431121199011154734",
		"hno": null,
		"house": "湖南省永州市",
		"pno": "0000000207120000603356"
	},
	{
		"unit": null,
		"num": 4,
		"sex": "1",
		"collflag": "0",
		"birday": "1989-07-28 00:00:00",
		"status": "未抓获",
		"name": "郭小坪",
		"idcard": "350212198907281553",
		"hno": null,
		"house": "后村村洞庭二210号",
		"pno": "0000000000000000112668"
	},
	{
		"unit": null,
		"num": 5,
		"sex": "1",
		"collflag": "0",
		"birday": "1962-05-23 00:00:00",
		"status": "未抓获",
		"name": "刘代权",
		"idcard": "522124196205230414",
		"hno": null,
		"house": "贵州省正安县石矸村大山组",
		"pno": "0000000000000000112453"
	}],
	"pages": null,
	"operates": null
}
```
