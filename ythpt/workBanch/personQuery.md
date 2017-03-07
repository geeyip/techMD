* 警综人员查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/list', {
	"pcdName": "SP_INT_API_SEL_CSE_PERSON_ALL",
	"pcdParamValMap": {"name":"马海波", "sex":"1", "no":"R3301","birdaymi":"1969-08-01"},
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
		"birthday": "1969-08-01 00:00:00",
		"sex": "1",
		"no": "R3301066200002016080491",
		"colnum": null,
		"idcard": "412925196908013410",
		"naplace": "河南省南阳市镇平县",
		"idecard": null,
		"ideflag": "0",
		"rownum": 1,
		"fileno": "T201703062454168",
		"creunit": "杭州市公安局西湖区分局转塘派出所",
		"cretime": "2016-12-01 08:22:48",
		"name": "马海波",
		"idename": null
	}],
	"pages": null,
	"operates": null
}
```

* 综采人员查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/list', {
	"pcdName": "SP_INT_API_SEL_SYN_PERSON_ALL",
	"pcdParamValMap": {"name":"陈莉莉","idcard":"511602199002053227"},
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
   		"birthday": "1990-02-05 00:00:00",
   		"sex": "2",
   		"no": "B3502067100002016060004",
   		"colnum": null,
   		"idcard": "511602199002053227",
   		"naplace": "四川省广安市广安区",
   		"idecard": null,
   		"ideflag": "0",
   		"rownum": 1,
   		"fileno": "T201703062018007",
   		"creunit": "厦门市公安局禾山派出所",
   		"cretime": "2016-06-01 09:41:20",
   		"name": "陈莉莉",
   		"idename": null
   	}],
   	"pages": null,
   	"operates": null
   }
```

* 指纹人员查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/list', {
	"pcdName": "SP_INT_API_SEL_HDP_PERSON_ALL",
	"pcdParamValMap": {"idcard":"362324197606303317","no":"350206721604157"},
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
    		"birthday": "1976-06-30 00:00:00",
    		"sex": "1",
    		"no": "350206721604157",
    		"colnum": 1,
    		"idcard": "362324197606303317",
    		"naplace": "江西省上饶地区铅山县",
    		"idecard": null,
    		"ideflag": "0",
    		"rownum": 1,
    		"fileno": "T20170306535333",
    		"creunit": null,
    		"cretime": "2016-04-26 00:00:00",
    		"name": "杨保军",
    		"idename": null
    	}],
    	"pages": null,
    	"operates": null
    }
```

* DNA人员查询接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/list', {
	"pcdName": "SP_INT_API_SEL_DNA_PERSON_ALL",
	"pcdParamValMap": {"no":"R3502000002008012800030","name":"吴霜"},
	"begin": "1",
	"end": "2"
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
   		"birthday": null,
   		"sex": "2",
   		"no": "R3502000002008012800030",
   		"colnum": null,
   		"idcard": "510214197708243421",
   		"naplace": null,
   		"idecard": null,
   		"ideflag": "0",
   		"rownum": 1,
   		"fileno": "T201703061499784",
   		"creunit": null,
   		"cretime": null,
   		"name": "吴霜",
   		"idename": null
   	}],
   	"pages": null,
   	"operates": null
   }
```


* 人员档案人员基本信息接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PERSON",
	"pcdParamValMap": {"fileno":"T201703062454137"}
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
		"source": null,
		"creunit": "杭州市公安局上城区分局湖滨派出所",
		"status": "抓获",
		"cretime": "2016-09-01 07:54:03",
		"name": "徐鸿怡",
		"faflag": "否",
		"idcard": "330103198101200018",
		"house": "杭州市下城区仙林苑３２幢２楼",
		"pno": "R3301025400002016080636"
	}],
	"pages": null,
	"operates": null
}
```

* 人员档案人员指纹信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PER_HANDPRINT",
	"pcdParamValMap": {"fileno":"T20170306725715"}
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
		"hjd": "云南省红河哈尼族彝族自治州泸西县石缸冲村46号",
		"faflag": "否",
		"sfzh": "532527199812062658",
		"nydw": "厦门市公安局大同派出所",
		"pno": "R3502127200002015101190",
		"ryxm": "代路程",
		"nyrq": null,
		"ryzwxx": "350212721510039"
	}],
	"pages": null,
	"operates": null
}
```

* 人员档案人员DNA信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PER_DNA",
	"pcdParamValMap": {"fileno":"T201703061570655"}
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
		"rybh": "R3502003202002015050034",
		"sjdw": null,
		"dno": "R3502000002015061736854",
		"hjd": "越南北江省陆岩县建成镇坡甘村",
		"faflag": "否",
		"sfzh": null,
		"sjsj": null,
		"ryxm": "NHU VAN HOU(茹文和）"
	}],
	"pages": null,
	"operates": null
}
```

* 人员档案比中信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PERSON_HIT_INFO",
	"pcdParamValMap": {"fileno":"T201703071499885"}
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
		"detail": "安溪县城厢镇经兜村移动通信店",
		"status": null,
		"cno": null,
		"kno": "K3505241203002009040006",
		"type": "DNA比中",
		"haptime": "2009-02-20 00:00:00",
		"kind": "入户盗窃案"
	}],
	"pages": null,
	"operates": null
}
```

* 人员档案被冒名信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_FALSED_PERSON",
	"pcdParamValMap": {"fileno":"T201703062052690"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：
{
	"flag": 1,
	"totalCount": 3,
	"msg": null,
	"data": [{
		"creunit": null,
		"cretime": "2004-04-07 00:00:00",
		"no": "A35021210004265386",
		"name": "林英灯",
		"idcard": "350221198111200590",
		"house": "马巷镇黎安村田边84号",
		"type": "综采"
	},
	{
		"creunit": "厦门市公安局马巷派出所",
		"cretime": "2013-09-11 15:41:30",
		"no": "R3502137200002013090067",
		"name": "林英灯",
		"idcard": "350221198111200590",
		"house": "福建省厦门市翔安区马巷镇黎安村田边84号",
		"type": "综采"
	},
	{
		"creunit": "厦门市公安局嘉莲派出所",
		"cretime": "2012-03-30 11:08:20",
		"no": "R3502038000002012030143",
		"name": "马学峰",
		"idcard": "350221198111200590",
		"house": "青海省门源回族自治县青石咀镇尕大滩村57号",
		"type": "综采"
	}],
	"pages": null,
	"operates": null
}
```

* 综采人员信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_SYN_PERSON",
	"pcdParamValMap": {"fileno":"T201703061683087"}
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
		"creunit": null,
		"cretime": "2005-03-23 00:00:00",
		"name": "周景平",
		"faflag": "否",
		"idcard": "350205194601011014",
		"house": "杏林村七组",
		"pno": null,
		"spno": "10000439"
	}],
	"pages": null,
	"operates": null
}
```

* 查询认证信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_IDENTIFY_PERSON",
	"pcdParamValMap": {"fileno":"T201703062454134"}
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
	"data": [{
		"birthday": "1976-06-11 00:00:00",
		"phone": null,
		"sex": null,
		"weight": null,
		"maflag": null,
		"edudegree": "技工学校",
		"dno": null,
		"alias": null,
		"preaddr": "杭州市拱墅区左岸花园９幢１单元３０１室",
		"idcard": "330702197606110415",
		"job": null,
		"pid": null,
		"house": "浙江省金华市婺城区",
		"nation": "汉族",
		"ideno": "I201703060000000004",
		"natity": "中国",
		"idetime": "2017-03-06 19:09:39",
		"ideby": "test",
		"height": 170,
		"name": "吴观孙",
		"flength": null,
		"feature": null,
		"ideunit": "350200000000",
		"house_cn": "杭州市拱墅区左岸花园９幢１单元３０１室"
	}],
	"pages": null,
	"operates": null
}
```

* 插入认证信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_INS_IDENTIFY_PERSON",
	"pcdParamValMap": {"birthday":"1989-02-05","sex":"1","phone":"12524444","weight":"65","maflag":"1","dno":"343545","foot":"43","preaddr":"杭州","alias":"张三","job":"海鑫","idcard":"431126199310010871","pid":"34fffsfds","house":"湖南","nation":"2","ideby":"李四","height":"125","fileno":"T34343435","housecn":"湖南","name":"张三","feature":"无","nality":"1","ideunit":"3502000000","calture":"2"}
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
	"data": "1",
	"pages": null,
	"operates": null
}
```

* 字典接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/dict', {
	"tableName":"T_CET_DICT_MARRY_STATUS"
},
function(res) {
	log(obj2str(res))
},
true)
//tableName备注：T_CET_DICT_NATION--民族，T_CET_DICT_NATIONALITY--国籍，T_CET_DICT_EDU_LEVEL--学历,
//T_CET_DICT_MARRY_STATUS--是否已婚
2.返回值格式：
{
	"flag": 1,
	"totalCount": 0,
	"msg": null,
	"data": [{
		"key": "0",
		"value": "未婚"
	},
	{
		"key": "1",
		"value": "已婚"
	},
	{
		"key": "9",
		"value": "未知"
	}],
	"pages": null,
	"operates": null
}
```

* 修改认证信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_UPD_IDENTIFY_PERSON",
	"pcdParamValMap": {"birthday":"1989-02-05","sex":"1","phone":"12524444","weight":"65","maflag":"1","dno":"343545","foot":"43","preaddr":"杭州","alias":"张三","job":"海鑫","idcard":"431126199310010871","pid":"34fffsfds","house":"湖南","nation":"2","ideby":"李四","height":"125","fileno":"T34343435","housecn":"湖南","name":"张三","feature":"无","nality":"1","ideunit":"3502000000","calture":"2"}
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
	"data": "1",
	"pages": null,
	"operates": null
}
```


* 串并情况接口

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/cba_info', {
	"ryNo": "R4403075500002013020350"
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
	"data": [{
		"id": "F34429BD68B900D2E0430A2833CF00D2",
		"createDate": "2013-11-02 00:00:00",
		"cbaid": "CB4403000000002014020376",
		"cbmc": null,
		"cbnum": "2",
		"rynum": "2",
		"cbr": null,
		"cbaType": "指纹",
		"cbdw": "广东省公安厅",
		"cblb": "入室盗窃(夜盗)"
	}],
	"pages": null,
	"operates": null
}
```

```java
字段说明：
警综人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
警综人员查询参数说明：{"unit":"录入单位","crtmin":"录入时间初值","sex":"性别","birdaymi":"出生日期初值","count":"行数","crtmax":"录入时间终值","no":"编号","name":"姓名","idcard":"身份证号","naplace":"籍贯","birdayma":"出生日期终值"}
综采人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
综采人员查询参数说明：{"unit":"录入单位","crtmin":"录入时间","sex":"性别","birdaymi":"出生日期","count":"行数","crtmax":"录入时间","no":"编号","name":"姓名","idcard":"身份证号","naplace":"籍贯","birdayma":"出生日期"}
指纹人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
指纹人员查询参数说明：{"unit":"捺印单位","crtmin":"捺印时间","sex":"性别","birdaymi":"出生日期","count":"行数","crtmax":"捺印时间","no":"编号","name":"姓名","idcard":"身份证号","naplace":"籍贯","birdayma":"出生日期"}
DNA人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
DNA人员查询参数说明：{"unit":"送检单位","crtmin":"送检时间","sex":"性别","birdaymi":"出生日期","count":"行数","crtmax":"送检时间","no":"编号","name":"姓名","idcard":"身份证号","naplace":"籍贯","birdayma":"出生日期"}
插入认证信息结果集说明：{}
插入认证信息参数说明：{"birthday":"出生日期","sex":"性别","phone":"联系电话","weight":"体重","maflag":"是否已婚","dno":"DNA编号","foot":"足长","preaddr":"现住址","alias":"别名","job":"工作单位","idcard":"身份证号","pid":"照片id","house":"户籍地字典","nation":"民族","ideby":"认证人","height":"身高","fileno":"档案编号","housecn":"户籍地详址","name":"姓名","feature":"其他体貌特征","nality":"国籍","ideunit":"认证单位","calture":"文化程度"}
查询认证信息结果集说明：{"birthday":"出生日期","sex":"性别","phone":"联系方式","weight":"体重","maflag":"是否已婚","edudegree":"文化程度","dno":"DNA编号","preaddr":"现住址","alias":"别名","job":"工作单位","idcard":"身份证号","pid":"照片","house":"户籍地","ideno":"认证编号","nation":"民族","natity":"国籍","idetime":"认证时间","ideby":"认证人","height":"身高","flength":"足长","name":"姓名","feature":"其他体貌特征","ideunit":"认证单位","house_cn":"户籍地详址"}
查询认证信息参数说明：{"fileno":"档案编号"}
人员档案人员基本信息结果集说明：{"source":"人员来源","creunit":"人员创建单位","status":"人员状态","cretime":"创建时间","name":"人员姓名","faflag":"是否冒名","idcard":"人员身份证","house":"人员户籍地","pno":"人员编号"}
人员档案人员基本信息参数说明：{"fileno":"档案编号"}
人员档案人员指纹信息结果集说明：{"hjd":"户籍地","faflag":"是否冒名","sfzh":"身份证号","nydw":"捺印单位","pno":"人员编号","nyrq":"捺印日期","ryxm":"人员姓名","ryzwxx":"人员指纹编号"}
人员档案人员指纹信息参数说明：{"fileno":"档案编号"}
人员档案人员DNA信息结果集说明：{"rybh":"警综人员编号","sjdw":"送检单位","dno":"DNA编号","hjd":"户籍地","faflag":"是否冒名","sfzh":"身份证号","sjsj":"送检时间","ryxm":"姓名"}
人员档案人员DNA信息参数说明：{"fileno":"档案编号"}
人员档案比中信息结果集说明：{"detail":"发案地点","status":"状态","cno":"案件编号","type":"类型","haptime":"发案日期","kno":"勘察编号","kind":"案件类别"}
人员档案比中信息参数说明：{"fileno":"档案编号"}
人员档案被冒名信息结果集说明：{"creunit":"录入单位","cretime":"录入时间","no":"编号","name":"姓名","idcard":"身份证号","house":"户籍地","type":"类型"}
人员档案被冒名信息参数说明：{"fileno":"档案编号"}
综采人员信息结果集说明：{"creunit":"创建单位","cretime":"创建时间","name":"姓名","faflag":"是否冒名","idcard":"身份证号","house":"户籍地","pno":"警综人员编号","spno":"综采人员编号"}
综采人员信息参数说明：{"fileno":"档案编号"}
串并情况结果集说明：{"createDate":"串并时间","cbaid":"串并号","cbmc":"串并名称","cbnum":"案件数量","rynum":"人员数量","cbaType":"串并依据","cbdw":"串并单位","cblb": "串并类别"}
串并情况参数说明：{"ryNo":"人员编号"}
```