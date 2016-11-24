## 案件信息标注API文档

* 案件信息标注查询接口（点击参数管理时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/case/list
	后端格式为/api/{recordLog}/xlbz/case/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_CASE_ALL_INFO",
                procedureParamValueList:
                [
                    {fieldName:'P_VC_CASE_NO_IN', value:''},//案件编号
                    {fieldName:'P_D_CREATE_TIME_MIN_IN', value:'2016-11-11 11:11:11'},//录入日期开始
                    {fieldName:'P_D_CREATE_TIME_MAX_IN', value:''},//录入日期结束
                    {fieldName:'P_VC_TAG_CASE_TYPE_IN', value:''},//小类案别
                    {fieldName:'P_VC_CASE_BRIEF_IN', value:''},//简要案情
                    {fieldName:'P_D_HAPPEN_TIME_MIN_IN', value:''},//案发时间开始
                    {fieldName:'P_D_HAPPEN_TIME_MAX_IN', value:''},//案发时间结束
                    {fieldName:'P_VC_CREATE_UNIT_IN', value:''},//管辖单位
                    {fieldName:'P_C_USURPATION_FLAG_IN', value:''},//是否侵财 1:侵财；0：非侵财
                    {fieldName:'P_VC_CASE_STATUS_IN', value:''},//案件状态
                    {fieldName:'P_N_RECORD_ORDER', value:''},//取值开始
                    {fieldName:'P_N_RECORD_COUNT', value:''}//取值截止
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 2,
        "msg": null,
        "data":
        [
            {
                "caseno": "",//案件编号
                "begin": "2016-11-11 11:11:11",//案发时间开始
                "end": "",//案发时间结束
                "area": "",//发案区划
                "address": "",//案发地点
                "kind": "",//案件类别
                "status": "",//案件状态
                "unit": "",//录入单位
                "casekind": "",//小类案别
                "means": "",//作案手段
                "flag": "",//待标注、已标注
                "order": ""//排序
            },
            {
                "caseno": "",//案件编号
                "begin": "2016-11-11 11:11:11",//案发时间开始
                "end": "",//案发时间结束
                "area": "",//发案区划
                "address": "",//案发地点
                "kind": "",//案件类别
                "status": "",//案件状态
                "unit": "",//录入单位
                "casekind": "",//小类案别
                "means": "",//作案手段
                "flag": "",//待标注、已标注
                "order": ""//排序
            }
        ],
        "pages": null,
        "operates": null
    }
```



- 案件抽查接口

```java
1.API路径：http://localhost:8090/api/1/xlbz/case/spot_check
	后端格式为/api/{recordLog}/xlbz/case/spot_check，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_CASE_CONTENT",
                procedureParamValueList:
                [
                    {fieldName:'P_CASE_NO_IN', value:'A3301855500002016090001'}//案件编号
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data":
        [
            {
                "content": ""//抽查内容
            }
        ],
        "pages": null,
        "operates": null
    }
```



- 案件标注查询接口（点击案件信息标注进入案件标注页面时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/case/info
	后端格式为/api/{recordLog}/xlbz/case/info，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_CASE_INFO",
                procedureParamValueList:
                [
                    {fieldName:'P_CASE_NO_IN', value:'A3301855500002016090001'}//案件编号
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data":
        [
            {
                "caseno": "",//案件编号
                "happentime": "",//案发时间
                "address": "",//案发地点
                "unit": "",//选择单位
                "solvetime": "",//破案时间
                "status": "",//案件状态
                "summary": "",//简要案情
                "casekind": "",//小类案别
                "means": ""//作案手段
            }
        ],
        "pages": null,
        "operates": null
    }
```



- 案件标注接口（点击案件标注页面的保存时触发）

```java
1.API路径：http://localhost:8090/api/1/xlbz/case/insert
	后端格式为/api/{recordLog}/xlbz/case/insert，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_INS_CASE_TAG",
                procedureParamValueList:
                [
                    {fieldName:'P_CASE_NO_IN', value:'A3301855500002016090001'},//案件编号
                    {fieldName:'P_CASE_TYPE_TAG_IN', value:''},//小类案别
                    {fieldName:'P_CASE_MEANS_TAG_IN', value:''}//作案手段
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 0,
        "msg": null,
        "data": "1",
        "pages": null,
        "operates": null
    }
```
