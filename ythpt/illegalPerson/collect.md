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
		pno: '',//人员编号
		hno: '',//指纹编号
		name: '',//姓名
		sex: '',//性别
		idcard: '',//出生日期
		place: '',//籍贯
		unit: '',//录入单位
		status: '',//人员状态
		collflag: '',//是否采集
		birdaymi: '',//出生日期最小
		birdayma: ''//出生日期最大
		lrsjma:'',//录入时间最大
		lrsjmi:''录入时间最小
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
		"hno": null,//指纹编号
		"house": "贵州省三穗县良上乡上寨村土地塘组",
		"pno": "R3506272305002009100007",
		 lrsj: "1899-12-30 09:00:00"//录入时间
	}],
	"pages": null,
	"operates": null
}
```
