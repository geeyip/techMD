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
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_OUT_RECORD_AMOUNT_OUT_NUMBER":"",//返回结果数量
            "P_CASE_INFO_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "D_HAPPEN_TIME_MIN_IN": "2016-11-11 11:11:11",//案发时间开始
                    "D_HAPPEN_TIME_MAX_IN": "",//案发时间结束
                    "VC_HAPPEN_AREA": "",//发案区划
                    "VC_HAPPEN_PLACE_DETAIL": "",//案发地点
                    "VC_CASE_KIND": "",//案件类别
                    "VC_CASE_STATUS": "",//案件状态
                    "VC_CREATE_UNIT": "",//录入单位
                    "VC_TAG_CASE_TYPE": "",//小类案别
                    "VC_TAG_CASE_CRI_MEANS": "",//作案手段
                    "C_TAG_FLAG": "",//待标注、已标注
                    "N_ROW_NUMBER": ""//排序
                },
                {
                    "D_HAPPEN_TIME_MIN_IN": "2016-11-11 11:11:11",//案发时间开始
                    "D_HAPPEN_TIME_MAX_IN": "",//案发时间结束
                    "VC_HAPPEN_AREA": "",//发案区划
                    "VC_HAPPEN_PLACE_DETAIL": "",//案发地点
                    "VC_CASE_KIND": "",//案件类别
                    "VC_CASE_STATUS": "",//案件状态
                    "VC_CREATE_UNIT": "",//录入单位
                    "VC_TAG_CASE_TYPE": "",//小类案别
                    "VC_TAG_CASE_CRI_MEANS": "",//作案手段
                    "C_TAG_FLAG": "",//待标注、已标注
                    "N_ROW_NUMBER": ""//排序
                }
            ]
        },
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
                    {fieldName:'P_CASE_NO_IN', value:''}//案件编号
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_CASE_INFO_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "VC_CASE_NO": "",//案件编号
                    "D_HAPPEN_BEGIN_TIME": "",//案发时间
                    "VC_HAPPEN_DETAIL": "",//案发地点
                    "VC_CREATE_UNIT": "",//选择单位
                    "D_SOLVE_TIME": "",//破案时间
                    "VC_CASE_STATUS": "",//案件状态
                    "VC_CASE_SUMMARY": "",//简要案情
                    "VC_TAG_CASE_KIND": "",//小类案别
                    "VC_TAG_CASE_CRI_MEANS": ""//作案手段
                }
            ]
        },
        "pages": null,
        "operates": null
    }
```
