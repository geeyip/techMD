## 侵财类案件统计API文档

* 小类案别发案情况查询接口

```java
1.API路径：http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/xlablist
	后端格式为xlcb/api/{recordLog}/tjkh/qcaj/xlablist，其中{recordLog}为前端传入，标识是否需要记录操作日志。
	前端格式:$post('http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/xlablist',{pcdName:"SP_TAG_API_SEL_REP_STATISTICS",
                     pcdParamValMap:{"timemin":"","timemax":"","timetype":"1","kind":""}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_STATISTICS",
                pcdParamValMap:{"timemin":"","timemax":"","timetype":"1","kind":""}
             }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "value": "合计",//本身中文
                "pvalue": "合计",//上级中文
                "key": "合计",//本身代码
                "pkey": "合计",//上级代码
                "accnum":"",//受理案件数
                "regnum":"",//立案数
                "regrat":"",//立案率
                "solnum":"",//破案数
                "solrat":""//破案率
            }
        ],
        "pages": null,
        "operates": null
    }
```


* 分县级发案情况查询接口

```java
1.API路径：http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/fxjlist
	后端格式为xlcb/api/{recordLog}/tjkh/qcaj/fxjlist，其中{recordLog}为前端传入，标识是否需要记录操作日志。
	前端格式:$post('http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/fxjlist',{pcdName:"SP_TAG_API_SEL_REP_REGION_CASE",
                     pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","unit":""}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_REGION_CASE",
                pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","unit":""}
             }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "unit": "",//单位代码
                "unitcn": "",//单位中文
                "accnum": "",//受理数
                "regnum": "",//立案数
                "regrat":"",//立案率
                "solnum":"",//破案数
                "solrat":""//破案率
            }
        ],
        "pages": null,
        "operates": null
    }
```


* 派出所发案情况查询接口

```java
1.API路径：http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/pcslist
	后端格式为xlcb/api/{recordLog}/tjkh/qcaj/pcslist，其中{recordLog}为前端传入，标识是否需要记录操作日志。
	前端格式:$post('http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/pcslist',{pcdName:"SP_TAG_API_SEL_REP_POLICE_CASE",
                     pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","unit":""}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_POLICE_CASE",
                pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","unit":""}
             }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "pkey": "",//区县代码
                "pvalue": "",//区县中文
                "key": "",//派出所代码
                "value": "",//派出中文
                "accnum":"",//案件受理数
                "regnum":"",//立案数
                "regrat":"",//立案率
                "solnum":"",//破案数
                "solrat":""//破案率
            }
        ],
        "pages": null,
        "operates": null
    }
```


