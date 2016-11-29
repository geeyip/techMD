## 案件抽查API文档

* 案件抽查报表查询接口

```java
1.API路径：http://localhost:8090/xlcb/api/0/tjkh/caseCheck/list
	后端格式为/xlcb/api/{recordLog}/tjkh/caseCheck/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_CASE_CHECK",
                pcdParamValMap:{'mintime':'', 'maxtime':''}//统计开始时间,统计结束时间
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":
        [
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "unitname": "",//单位中文
                "caseno": "",//案件编号
                "rate": "",//准确率
                "score": ""//得分
            },
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "caseno": "",//案件编号
                "rate": "",//准确率
                "score": ""//得分
            }
        ],
        "pages": null,
        "operates": null
    }
```

