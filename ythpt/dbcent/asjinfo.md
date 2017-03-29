* 案事件列表接口

```java
1.  前端调用:
$.post('http://192.168.1.211:47000//datacenter/api/apiService', {
	jsonStr: '{"userName":"ythpt","userPassword":"ythpt","begin":"0","end":"60","pcdName":"SP_INT_API_SEL_CASE_EVENT_INFO","pcdParamValMap":{"actimema":"受理时间","rno":"警情编号","detail":"案发地点","sunit":"主办人","maflag":"是否存入原始资料库","sno":"现勘编号","reunit":"接警单位","hatimemi":"案发时间","laflag":"是否送检","actimemi":"受理时间","cno":"案件编号","ckind":"案件类别","accunit":"受理单位","sflag":"是否勘验","retimema":"接警时间","buflag":"是否串并","rekind":"警情类别","retimemi":"接警时间","cflag":"是否立案","hatimema":"案发时间"}}'
},
function(res) {
	console.log(obj2str(res))
})
2.返回值格式：
{
	"data": [{
		"region": "案发区划",
		"rno": "警情编号",
		"detail": "案发地点",
		"sno": "现勘编号",
		"lflag": "是否送检",
		"rkindcn": "接警类别中文",
		"rkind": "接警类别",
		"runitcn": "接警单位中文",
		"rownum": "序号",
		"statuscn": "案件状态中文",
		"acunitcn": "受理单位中文",
		"sflag": "是否勘验",
		"rtime": "接警时间",
		"mflag": "是否存入原始资料库",
		"runit": "接警单位",
		"sid": "现勘ID",
		"sunit": "主办单位",
		"hatime": "案发时间",
		"ckindcn": "案件类别中文",
		"status": "案件状态",
		"cno": "案件编号",
		"bflag": "是否串并",
		"sunitcn": "主办单位中文",
		"fno": "档案编号",
		"ckind": "案件类别",
		"regioncn": "案发区划中文",
		"actime": "受理时间",
		"cname": "案件名称",
		"acunit": "受理单位"
	}],
	"flag": 1,
	"totalCount": 1
}
```