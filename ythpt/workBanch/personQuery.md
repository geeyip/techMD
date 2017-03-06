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
	"pcdParamValMap": {"fileno":"T201703061499784"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 人员档案人员指纹信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PER_HANDPRINT",
	"pcdParamValMap": {"fileno":"T201703061499784"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 人员档案人员DNA信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PER_DNA",
	"pcdParamValMap": {"fileno":"T201703061499784"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 人员档案比中信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_PERSON_HIT_INFO",
	"pcdParamValMap": {"fileno":"T201703061499784"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 人员档案被冒名信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_FALSED_PERSON",
	"pcdParamValMap": {"fileno":"T201703061499784"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 综采人员信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_SYN_PERSON",
	"pcdParamValMap": {"fileno":"T201703061499784"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 查询认证信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_SEL_IDENTIFY_PERSON",
	"pcdParamValMap": {"no":""}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```

* 插入认证信息

```java
1.  前端调用:
$post('http://localhost:8090/api/0/workbench/person_query/info', {
	"pcdName": "SP_INT_API_INS_IDENTIFY_PERSON",
	"pcdParamValMap": {"birthday":"出生日期","sex":"1","phone":"5433265","dno":"DNA编号","foot":"足长","alias":"别名","preaddr":"杭州","job":"海鑫","idcard":"431126199310010871","house":"户籍地","nation":"民族","ideby":"认证人","flag":"标识","height":"身高","name":"姓名","nality":"国籍","ideunit":"认证单位","calture":"文化程度"}
},
function(res) {
	log(obj2str(res))
},
true)
2.返回值格式：

```


```java
字段说明：
警综人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
警综人员查询参数说明：{"sex":"性别","count":"行数","no":"编号","idcard":"身份证号","naplace":"籍贯","amount":"总数","crtmin":"录入时间初值","unit":"录入单位","flag":"标识","birdaymi":"出生日期初值","crtmax":"录入时间终值","name":"姓名","birdayma":"出生日期终值","perinfo":"人员信息"}
综采人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
综采人员查询参数说明：{"sex":"性别","count":"行数","no":"编号","idcard":"身份证号","naplace":"籍贯","amount":"总数","crtmin":"录入时间","unit":"录入单位","flag":"标识","birdaymi":"出生日期","crtmax":"录入时间","name":"姓名","birdayma":"出生日期","perinfo":"人员信息"}
指纹人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
指纹人员查询参数说明：{"sex":"性别","count":"行数","no":"编号","idcard":"身份证号","naplace":"籍贯","amount":"总数","crtmin":"捺印时间","unit":"捺印单位","flag":"标识","birdaymi":"出生日期","crtmax":"捺印时间","name":"姓名","birdayma":"出生日期","perinfo":"人员信息"}
DNA人员查询结果集说明：{"birthday":"出生日期","sex":"性别","no":"编号","idcard":"身份证号","colnum":"采集数量","naplace":"户籍地","idecard":"认证身份证号","ideflag":"认证标识","rownum":"序号","fileno":"档案编号","creunit":"录入单位","cretime":"录入时间","name":"姓名","idename":"认证姓名"}
DNA人员查询参数说明：{"sex":"性别","count":"行数","no":"编号","idcard":"身份证号","naplace":"籍贯","amount":"总数","crtmin":"送检时间","unit":"送检单位","flag":"标识","birdaymi":"出生日期","crtmax":"送检时间","name":"姓名","birdayma":"出生日期","perinfo":"人员信息"}
插入认证信息结果集说明：{}
插入认证信息参数说明：{"birthday":"出生日期","sex":"性别","phone":"联系电话","weight":"体重","maflag":"是否已婚","dno":"DNA编号","foot":"足长","preaddr":"现住址","alias":"别名","job":"工作单位","idcard":"身份证号","pid":"照片id","house":"户籍地字典","nation":"民族","ideby":"认证人","flag":"标识","height":"身高","housecn":"户籍地详址","name":"姓名","feature":"其他体貌特征","nality":"国籍","ideunit":"认证单位","calture":"文化程度"}
查询认证信息结果集说明：{"birthday":"出生日期","sex":"性别","phone":"联系方式","weight":"体重","maflag":"是否已婚","edudegree":"文化程度","dno":"DNA编号","preaddr":"现住址","alias":"别名","job":"工作单位","idcard":"身份证号","pid":"照片","house":"户籍地","ideno":"认证编号","nation":"民族","natity":"国籍","idetime":"认证时间","ideby":"认证人","height":"身高","flength":"足长","name":"姓名","feature":"其他体貌特征","ideunit":"认证单位","house_cn":"户籍地详址"}
查询认证信息参数说明：{"ideinfo":"认证信息","flag":"标识","no":"编号","type":"数据类型"}
人员档案人员基本信息结果集说明：{"source":"人员来源","creunit":"人员创建单位","status":"人员状态","cretime":"创建时间","name":"人员姓名","faflag":"是否冒名","idcard":"人员身份证","house":"人员户籍地","pno":"人员编号"}
人员档案人员基本信息参数说明：{"amount":"总数","flag":"标识","fileno":"档案编号","ryxx":"人员信息"}
人员档案人员指纹信息结果集说明：{"hjd":"户籍地","faflag":"是否冒名","sfzh":"身份证号","nydw":"捺印单位","pno":"人员编号","nyrq":"捺印日期","ryxm":"人员姓名","ryzwxx":"人员指纹编号"}
人员档案人员指纹信息参数说明：{"amount":"总数","flag":"标识","fileno":"档案编号","ryzwxx":"人员指纹信息"}
人员档案人员DNA信息结果集说明：{"rybh":"警综人员编号","sjdw":"送检单位","dno":"DNA编号","hjd":"户籍地","faflag":"是否冒名","sfzh":"身份证号","sjsj":"送检时间","ryxm":"姓名"}
人员档案人员DNA信息参数说明：{"amount":"总数","flag":"标识","fileno":"档案编号","dnainfo":"DNA信息"}
人员档案比中信息结果集说明：{"detail":"发案地点","status":"状态","cno":"案件编号","type":"类型","haptime":"发案日期","kno":"勘察编号","kind":"案件类别"}
人员档案比中信息参数说明：{"amount":"总数","flag":"标识","fileno":"档案编号","hitinfo":"比中信息"}
人员档案被冒名信息结果集说明：{"creunit":"录入单位","cretime":"录入时间","no":"编号","name":"姓名","idcard":"身份证号","house":"户籍地","type":"类型"}
人员档案被冒名信息参数说明：{"amount":"总数","flag":"标识","fileno":"档案编号","ryxx":"人员信息"}
综采人员信息结果集说明：{"creunit":"创建单位","cretime":"创建时间","name":"姓名","faflag":"是否冒名","idcard":"身份证号","house":"户籍地","pno":"警综人员编号","spno":"综采人员编号"}
综采人员信息参数说明：{"amount":"总数","flag":"标识","fileno":"档案编号","ryxx":"人员信息"}
```