## 侵财类案件统计API文档

* 小类案别发案情况查询接口

```java
1.API路径：http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/xlablist
	后端格式为xlcb/api/{recordLog}/tjkh/qcaj/xlablist，其中{recordLog}为前端传入，标识是否需要记录操作日志。
	前端格式:$post('http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/xlablist',{pcdName:"SP_TAG_API_SEL_REP_STATISTICS",
                     pcdParamValMap:{"timemin":"","timemax":"","timetype":"1","kind":"","unit":""}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_STATISTICS",
                pcdParamValMap:{"timemin":"","timemax":"","timetype":"1","kind":"","unit":""}
             }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "value": "",//本身中文
                "pvalue": "",//上级中文
                "key": "",//本身代码
                "pkey": "",//上级代码
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
                     pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","kind":"","unit":""}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_REGION_CASE",
                pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","kind":"","unit":""}
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
                     pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","kind":"","unit":""}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_POLICE_CASE",
                pcdParamValMap:{"timetype":"1","timemin":"","timemax":"","kind":"","unit":""}
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


* 侵财案件详细查看接口

```java
1.API路径：http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/view
	后端格式为xlcb/api/{recordLog}/tjkh/qcaj/view，其中{recordLog}为前端传入，标识是否需要记录操作日志。
	前端格式:$post('http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/view',{pcdName:"SP_TAG_API_SEL_CASE_BRIEF",
        pcdParamValMap:{'timemin':'2016-01-01', 'timemax':'', 'timetype':'1', 'kind':'', 'condit':'', 'unit':'',
        "reptype":"1",'order':'', 'record':''}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:'SP_TAG_API_SEL_CASE_BRIEF',
                                pcdParamValMap:{
                                    'timemin':'2016-01-01',//起始时间
                                    'timemax':'',
                                    'timetype':'1',//时间类型
                                    'kind':'',//当前类别
                                    'condit':'',//列类型,3.受理 2.立案 1.破案
                                    'unit':'',//当前单位
                                    'reptype':'',//报表类型 1.案别发案2.分县局、派出所发案
                                    'order':'',//第几行
                                    'record':''//要查的行数
                                }
             }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "brief": "2016年08月31日16时55分接巫华军报案称：2016年04月28日上午，卢正（320823197608180877，18258
                    160402）在向其公司（盈通汽车服务有限公司，位于滨江区长河街道中兴社区信雅达国际1-806）租赁一辆白色本
                    田杰德汽车（牌照浙A237VK）后......",
                "caseno": "A3301085200002016080146",
                "soldate": "2016-09-01 16:55:00",//破案时间
                "xh":"1",//行号
                "regdate":""//录入时间
            }
        ],
        "pages": null,
        "operates": null
    }
```


