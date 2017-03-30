* 案件关联现场

```java
1.  前端调用:
$.post('http://192.168.1.151:8023/datacenter/api/business/proc/apiInside/SP_INT_API_SEL_EVT_SOME_SCENE', {
	"fout":"案件编号"
},
function(res) {
	console.log(obj2str(res))
})
2.返回值格式：
{
	"data": [{
		"sno": "现场编号",
		"name": "勘验人",
		"matime": "勘验时间开始",
		"mitime": "勘验时间结束",
		"content": "勘验情况",
		"rownum": "序号"
	}],
	"flag": 1,
	"totalCount": 1
}
```