* 案件关联现场

```java
1.  前端调用:
$.post('http://192.168.1.211:47000/datacenter/api/business/proc/apiInside', {
	"fout":"案件编号"
},
function(res) {
	console.log(obj2str(res))
})
2.返回值格式：
{
	"data": [{
		"sno": "现勘编号",
		"name": "案件名称",
		"brief": "简要案情",
		"rownum": "序号"
	}],
	"flag": 1,
	"totalCount": 1
}
```