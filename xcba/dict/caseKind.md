## 案件类别字典API文档

* 案件类别字典查询接口（点击案件类别时触发）

```java
1.API路径：http://localhost:8090/api/0/dict/case_kind
	后端格式为/api/{recordLog}/dict/case_kind，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_INS_WEB_CASE_KIND"
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_CASE_KIND_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "parentkey": "502",//父字典代码
                    "key": "5020015",//字典代码
                    "value": "盗窃破坏城市公用设施",//字典值
                    "type": "C"//类型 A:大类,B:小类,C:手段
                },
                {
                    "parentkey": "502",//父字典代码
                    "key": "5020017",//字典代码
                    "value": "盗窃挖掘机电脑板",//字典值
                    "type": "C"//类型 A:大类,B:小类,C:手段
                }
            ]
        },
        "pages": null,
        "operates": null
    }
```

