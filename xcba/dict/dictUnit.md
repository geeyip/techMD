## 录入单位字典API文档

* 录入单位字典查询接口（点击录入单位时触发）

```java
1.API路径：http://localhost:8090/api/0/dict/dict_unit
	后端格式为/api/{recordLog}/dict/dict_unit，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_DICT_UNIT"
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":
        [
            {
                "prkey": "330110000000",//父字典代码
                "key": "330110520000",//字典代码
                "name": "杭州市公安局余杭区分局东湖派出所",//字典值
                "type": "B"//类型 A:分局,B:派出所,C:社区
            },
            {
                "prkey": "330110000000",//父字典代码
                "key": "330110550000",//字典代码
                "name": "杭州市公安局余杭区分局运河派出所",//字典值
                "type": "B"//类型 A:分局,B:派出所,C:社区
            }
        ],
        "pages": null,
        "operates": null
    }
```

