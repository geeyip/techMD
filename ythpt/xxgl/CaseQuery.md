* 警情查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_REC_CASE_ALL",
	"pcdParamValMap": {"no":"J350182720000201401000001"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": null,
		"rownum": 1,
		"detail": "金沙港",
		"hatime": "2014-01-01 02:06:25",
		"fileno": "T350200201703070013730287",
		"cretime": "2014-01-01 02:04:05",
		"no": "J350182720000201401000001",
		"cname": null,
		"kind": null
	}],
	"pages": null,
	"operates": null
}
```

* 案件查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_CSE_CASE_ALL",
	"pcdParamValMap": {"no":"A330103045500002009080977"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": null,
		"rownum": 1,
		"detail": "黄石镇水南村石兴街",
		"hatime": "2099-08-10 09:08:00",
		"fileno": "T350200201703070000436372",
		"cretime": "2010-03-26 11:12:31",
		"no": "A330103045500002009080977",
		"cname": null,
		"kind": null
	}],
	"pages": null,
	"operates": null
}
```

* 现勘查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_SCN_CASE_ALL",
	"pcdParamValMap": {"no":"K3505830000002016090827"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": null,
		"rownum": 1,
		"detail": "乐峰镇厚阳村坑内9组",
		"hatime": "2016-09-27 00:00:00",
		"fileno": "T350200201703070000645468",
		"cretime": "2016-09-27 09:07:00",
		"no": "K3505830000002016090827",
		"cname": null,
		"kind": "盗窃牲畜案"
	}],
	"pages": null,
	"operates": null
}
```

* 指纹查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_HDP_CASE_ALL",
	"pcdParamValMap": {"no":"xmhc160112003007"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": "厦门市公安局新阳派出所",
		"rownum": 1,
		"detail": "厦门市海沧区霞阳西路186号",
		"hatime": "2016-12-12 10:10:10",
		"fileno": "T350200201703070011625431",
		"cretime": "2016-12-13 10:20:20",
		"no": "xmhc160112003007",
		"cname": null,
		"kind": "入户盗窃案"
	}],
	"pages": null,
	"operates": null
}
```

* dna查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_DNA_CASE_ALL",
	"pcdParamValMap": {"no":"W3502000002016092810121"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": null,
		"rownum": 1,
		"detail": null,
		"hatime": "2016-09-11 00:00:00",
		"fileno": "T350200201703070004016217",
		"cretime": "2016-09-12 00:00:00",
		"no": "W3502000002016092810121",
		"cname": "20160911思明区东明路26号1902室A号房被盗",
		"kind": null
	}],
	"pages": null,
	"operates": null
}
```

* 足迹查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_FTP_CASE_ALL",
	"pcdParamValMap": {"no":"K350582240006201610008401"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": null,
		"rownum": 1,
		"detail": "晋江市西园街道赖厝社区雁山寺",
		"hatime": "2016-10-06 08:00:00",
		"fileno": "T350200201703070011134359",
		"cretime": null,
		"no": "K350582240006201610008401",
		"cname": null,
		"kind": null
	}],
	"pages": null,
	"operates": null
}
```

* 物证查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/list', {
	"pcdName": "SP_INT_API_SEL_PRV_CASE_ALL",
	"pcdParamValMap": {"no":"W35058224000620160900684"},
	"begin": "1",
	"end": "60"
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"unit": null,
		"rownum": 1,
		"detail": "福建省晋江市新塘街道新塘园阳泉服饰厂436宿舍",
		"hatime": "2016-09-26 08:00:00",
		"fileno": "T350200201703070009352359",
		"cretime": null,
		"no": "W35058224000620160900684",
		"cname": "2016-09-26 08:00福建省晋江市新塘街道新塘园阳泉服饰厂436宿舍入室盗窃案",
		"kind": "入户盗窃案"
	}],
	"pages": null,
	"operates": null
}
```

* 勘验信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_SCENE",
	"pcdParamValMap": {"fileno":"T350200201703070011620917"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"lotude": null,
		"sno": "K3505830000002010050070",
		"inperson": "吕金星,文学",
		"location": "居民小区",
		"sceaddr": "福建省南安市溪美街普东巷11幢302室",
		"inway": "从门侵入",
		"latude": null,
		"means": null,
		"goods": "笔记本电脑,外套",
		"content": null,
		"rownum": 1,
		"unit": null,
		"time": "2010-04-30 18:30:00",
		"value": "320",
		"cripoint": "结伙作案",
		"critime": "夜"
	}],
	"pages": null,
	"operates": null
}
```

* 现场dna信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_SCENE_DNA",
	"pcdParamValMap": {"fileno": "T350200201703070004016217"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"position": null,
		"unit": null,
		"dno": "W3502000002016092810121",
		"name": "20160911思明区东明路26号1902室A号房被盗",
		"type": "其他",
		"labno": "2016A2740-001",
		"coltime": "2016-09-12 00:00:00",
		"colby": "唐玮玮"
	}],
	"pages": null,
	"operates": null
}
```

* 现场足迹接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_SCENE_FOOTPRINT",
	"pcdParamValMap": {"fileno":"T350200201703070011850062"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"left": "礼盒下方地面",
		"type": "鞋印",
		"fno": "K350519000000201501007505",
		"colunit": null,
		"coltime": null,
		"colby": null
	}],
	"pages": null,
	"operates": null
}
```

* 警情信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_RECEPTION",
	"pcdParamValMap": {"fileno":"T350200201703070011625429"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 0,
	"msg": null,
	"data": [],
	"pages": null,
	"operates": null
}
```

* 现场指纹信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_SCENE_HANDPRINT",
	"pcdParamValMap": {"fileno": "T350200201703070011625429"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"detail": "同安区新民镇凤南大埔路48号中通快递公司",
		"hatime": null,
		"colunit": "厦门市公安局同安分局刑事侦查大队技术科",
		"left": "纸盒",
		"hno": "XM003L1604260003",
		"coltime": null,
		"kind": "盗窃案",
		"colby": "张题，邱福生"
	}],
	"pages": null,
	"operates": null
}
```

* 案件信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_CASE_INFO",
	"pcdParamValMap": {"fileno":"T350200201703070011136867"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"summary": "2010年1月21日19时50分，我所接到方建（江西南昌市新建县石埠乡田垅村，身份证号：360122198807291219）报案：2010年1月21日8时许，其把一部五羊本田摩托车停放在兴泰开发区鸿鑫财富广场“开心网吧”后面的租房楼下，后回租房休息。1月21日19时40分发现其停放在租房楼下的摩托车被盗。该车未上牌，车架号：261038002；发动机号：02598。该车于2006年购买，价值约4000元。",
		"rno": null,
		"detail": "鸿鑫广场开心网吧后面",
		"status": null,
		"hadate": "2010-01-21 08:00:00",
		"cno": "A3301257600002010010020",
		"kind": "盗窃摩托车案",
		"redate": null,
		"sodate": null,
		"unit": null,
		"place": "福建省漳州市长泰县",
		"user": "370120",
		"cname": null
	}],
	"pages": null,
	"operates": null
}
```

* 涉案比中信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_CASE_HIT_INFO",
	"pcdParamValMap": {"fileno":"T350200201703070011625468"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"ryly": null,
		"lrsj": "2016-05-09 09:28:15",
		"hjd": "贵州省铜仁地区印江土家族苗族自治县峨岭镇麻柳村水井堡组",
		"ryzt": "未抓获",
		"sfzh": "522226199609290036",
		"pno": "R3502122400002016040017",
		"ryxm": "柳远锋",
		"lx": "指纹比中"
	}],
	"pages": null,
	"operates": null
}
```

* 提取物品接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_PROOF",
	"pcdParamValMap": {"fileno":"T350200201703070011892229"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"colpart": "北侧距离员工宿舍楼17.7m，东侧距离管理宿舍楼4.6m",
		"flag": null,
		"colway": "擦拭提取",
		"name": "血液（斑）",
		"type": null,
		"pno": "W35058224000620160300266",
		"coltime": null,
		"colby": null
	}],
	"pages": null,
	"operates": null
}
```

* 物证保管接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/info', {
	"pcdName": "SP_INT_API_SEL_PROOF_SAVE",
	"pcdParamValMap": {"fileno":"T350200201703070011892229"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 1,
	"msg": null,
	"data": [{
		"status": "4",
		"cretime": "2016-03-11 22:46:08",
		"name": "血液（斑）",
		"purpose": null,
		"type": "入库",
		"pno": "W35058224000620160300193",
		"billno": "B35058224000620160300082"
	}],
	"pages": null,
	"operates": null
}
```

* 串并情况接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/xxgl/case_query/cba_info', {
	"caseNo": "A4403068400002014010027",
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 0,
	"msg": null,
	"data": {
		"id": "ED886582B6FE00CAE0430A2833CF00CA",
		"createDate": "2013-03-15 00:00:00",
		"cbaid": "CB4403000000002013120318",
		"cbmc": "dddd",
		"cbnum": "4",
		"rynum": "1",
		"cbr": null,
		"cbaType": "DNA",
		"cbdwdm": null,
		"createDateStr": null,
		"paNum": null,
		"cbdw": "深圳市公安局",
		"cblb": "盗窃"
	},
	"pages": null,
	"operates": null
}
```

```java
字段说明：
警情查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
警情查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
案件查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
案件查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
现勘查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
现勘查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
指纹查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
指纹查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
dna查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
dna查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
足迹查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
足迹查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
物证查询结果集说明：{"rownum":"排序序号","unit":"录入单位","detail":"案发地点","hatime":"案发时间","fileno":"档案编号","cretime":"录入时间","no":"编号","kind":"案件类别","cname":"案件名称"}
物证查询参数说明：{"region":"案发区划","htimema":"案发时间终值","no":"编号","htimemi":"案发时间初值","kind":"案件类别"}
勘验信息结果集说明：{"lotude":"经度","sno":"现勘编号","inperson":"勘验人","location":"选择场所","sceaddr":"勘验地点","latude":"纬度","inway":"侵入方式","means":"作案手段","goods":"损失物品","content":"作案过程分析","rownum":"排序序号","unit":"勘验单位","time":"勘验时间","value":"损失价值","cripoint":"作案特点","critime":"选择时机"}
勘验信息参数说明：{"fileno":"档案编号"}
现场dna信息结果集说明：{"position":"提取部位","unit":"提取单位","dno":"DNA编号","name":"案件名称","type":"样本类型","labno":"实验室编号","coltime":"提取时间","colby":"提取人"}
现场dna信息参数说明：{"fileno":"档案编号"}
现场足迹信息结果集说明：{"colunit":"采集单位","left":"遗留位置","type":"足迹类型","fno":"足迹编号","coltime":"采集时间","colby":"采集人"}
现场足迹信息参数说明：{"fileno":"档案编号"}
警情信息结果集说明：{"rno":"警情编号","rectime":"接警时间","hatime":"案发时间","recunit":"接警单位","name":"警情名称","brief":"简要案情"}
警情信息参数说明：{"fileno":"档案编号"}
现场指纹信息结果集说明：{"detail":"发案地点","hatime":"发案时间","colunit":"提取单位","left":"遗留部位","hno":"指纹编号","coltime":"提取时间","kind":"案件类别","colby":"提取人"}
现场指纹信息参数说明：{"fileno":"档案编号"}
案件信息结果集说明：{"summary":"简要案情","unit":"主办单位","rno":"警情编号","detail":"发案地点","status":"案件状态","hadate":"发案时间","cno":"案件编号","place":"发案区划","user":"主办人","redate":"立案时间","kind":"案件类别","cname":"案件名称","sodate":"破案时间"}
案件信息参数说明：{"fileno":"档案编号"}
涉案比中信息结果集说明：{"ryly":"人员来源","lrsj":"录入时间","hjd":"户籍地","ryzt":"人员状态","sfzh":"身份证号","pno":"人员编号","lx":"类型","ryxm":"人员姓名"}
涉案比中信息参数说明：{"fileno":"档案编号"}
提取物品结果集说明：{"colpart":"提取部位","flag":"保管状态","colway":"提取方法","name":"物证名称","type":"物证类型","pno":"物证编号","coltime":"提取时间","colby":"提取人"}
提取物品参数说明：{"fileno":"档案编号"}
物证保管结果集说明：{"status":"清单状态","cretime":"申请时间","name":"物证名称","purpose":"清单用途","type":"清单类型","billno":"清单编号","pno":"物证编号"}
物证保管参数说明：{"fileno":"档案编号"}
串并情况结果集说明：{"createDate":"串并时间","cbaid":"串并号","cbmc":"串并名称","cbnum":"案件数量","rynum":"人员数量","cbaType":"串并依据","cbdw":"串并单位","cblb": "串并类别"}
串并情况参数说明：{"caseNo":"案件编号"}
```