* 获取提取物品列表接口

```java
1.  前端调用:
$.post('http://192.168.1.211:47000//datacenter/api/apiService', {
	jsonStr: '{"userName":"ythpt","userPassword":"ythpt","begin":"0","end":"60","pcdName":"SP_INT_API_SEL_SCN_MATERIAL","pcdParamValMap":{"collectBy":"提取人","collectTimeBegin":"提取时间初值","collectTimeEnd":"提取时间终值","collectUnit":"提取单位","kno":"现勘编号"}}'
2.返回值格式：
{
	"data": [{
		"collectBy": "提取人",
		"amount": "提取数量",
		"id": "物证id",
		"rownum": "序号",
		"unit": "提取单位",
		"collectTime": "提取时间",
		"photoId": "照片id",
		"name": "物证名称",
		"kno": "现勘编号"
	}],
	"flag": 1,
	"totalCount": 1
}
```