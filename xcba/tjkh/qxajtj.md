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


* 侵财案件详细查看接口

```java
1.API路径：http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/view
	后端格式为xlcb/api/{recordLog}/tjkh/qcaj/view，其中{recordLog}为前端传入，标识是否需要记录操作日志。
	前端格式:$post('http://192.168.1.120:8020/xlcb/api/0/tjkh/qcaj/view',{pcdName:"SP_TAG_API_SEL_CASE_BRIEF",
                      pcdParamValMap:{'timemin':'2016-01-01', 'timemax':'', 'timetype':'1', 'kind':'', 'unit':''}},o=>info(o),true)
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:'SP_TAG_API_SEL_CASE_BRIEF',
                                pcdParamValMap:{
                                    'timemin':'2016-01-01',//起始时间
                                    'timemax':'',
                                    'timetype':'1',//时间类型
                                    'kind':'',//当前类别
                                    'unit':''//当前单位
                                }
             }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": [
            {
                "brief": "2016年08月31日16时55分接巫华军报案称：2016年04月28日上午，卢正（320823197608180877，18258160402）在向其公司（盈通汽车服务有限公司，位于滨江区长河街道中兴社区信雅达国际1-806）租赁一辆白色本田杰德汽车（牌照浙A237VK）后，于8月21日19点23分在江苏省苏州市相城区阳澄湖西路出现后GPS信号消失。现无法联系到卢正及其女友（赵尧丽，手机号13735526101），损失价值140000元。",
                "caseno": "A3301085200002016080146",
                "soldate": "2016-09-01 16:55:00",
                "xh":"1",
                "regdate":""
            }
        ],
        "pages": null,
        "operates": null
    }
```


