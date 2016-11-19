## 人员信息标注API文档

* 人员信息标注查询接口（点击参数管理时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/person/list
	后端格式为/api/{recordLog}/xlbz/person/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_PERSON_ALL_INFO",
                procedureParamValueList:
                [
                    {fieldName:'P_VC_PERSON_NO_IN', value:''},//人员编号
                    {fieldName:'P_D_CREATE_TIME_MIN_IN', value:'2016-11-11 11:11:11'},//录入日期开始
                    {fieldName:'P_D_CREATE_TIME_MAX_IN', value:''},//录入日期结束
                    {fieldName:'P_VC_TAG_P_CASE_TYPE_IN', value:''},//小类案别
                    {fieldName:'P_VC_PERSON_TYPE_IN', value:''},//人员类别 0：犯罪；1：违法
                    {fieldName:'P_D_CAPTURE_TIME_MIN_IN', value:''},//抓获日期开始
                    {fieldName:'P_D_CAPTURE_TIME_MAX_IN', value:''},//抓获日期结束
                    {fieldName:'P_VC_CREATE_UNIT_IN', value:''},//管辖单位
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
            "P_PERSON_INFO_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "VC_CAPTURE_UNIT": "2016-11-11 11:11:11",//抓获单位
                    "VC_HAPPEN_AREA": "",//发案区划
                    "D_CAPTURE_TIME": "",//抓获日期
                    "VC_PERSON_TYPE": "",//人员类别
                    "VC_NAME": "",//姓名
                    "VC_ID_CARD_NO": "",//身份证号
                    "VC_HOUSEHOLD_DETAIL": "",//户籍地详址
                    "VC_PERS_CASE_KIND": "",//案件类别
                    "VC_PERS_CASE_KIND2": "",//案件类别1
                    "VC_TAG_P_CASE_KIND": "",//小类案别
                    "VC_TAG_PERSON_CRI_MEANS": "",//作案手段
                    "C_TAG_FLAG": "",//待标注、已标注
                    "N_ROW_NUMBER": ""//排序
                },
                {
                    "VC_CAPTURE_UNIT": "2016-11-11 11:11:11",//抓获单位
                    "VC_HAPPEN_AREA": "",//发案区划
                    "D_CAPTURE_TIME": "",//抓获日期
                    "VC_PERSON_TYPE": "",//人员类别
                    "VC_NAME": "",//姓名
                    "VC_ID_CARD_NO": "",//身份证号
                    "VC_HOUSEHOLD_DETAIL": "",//户籍地详址
                    "VC_PERS_CASE_KIND": "",//案件类别
                    "VC_PERS_CASE_KIND2": "",//案件类别1
                    "VC_TAG_P_CASE_KIND": "",//小类案别
                    "VC_TAG_PERSON_CRI_MEANS": "",//作案手段
                    "C_TAG_FLAG": "",//待标注、已标注
                    "N_ROW_NUMBER": ""//排序
                }
            ]
        },
        "pages": null,
        "operates": null
    }
```



- 人员标注查询接口（点击人员信息标注进入人员标注页面时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/person/info
	后端格式为/api/{recordLog}/xlbz/person/info，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_PERSON_INFO",
                procedureParamValueList:
                [
                    {fieldName:'P_PERSON_NO_IN', value:''}//人员编号
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_PERSON_INFO_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "VC_PERSON_NO": "",//人员编号
                    "VC_SEX": "",//性别
                    "VC_NAME": "",//姓名
                    "VC_ID_CARD_NO": "",//身份证号
                    "VC_HOUSEHOLD_DETAIL": "",//户籍地
                    "D_CAPTURE_TIME": "",//抓获时间
                    "VC_TAG_P_CASE_KIND": "",//小类案别
                    "VC_TAG_PERSON_CRI_MEANS": "",//作案手段
                    "VC_CRIMINAL_DETAIL": ""//违法犯罪情况
                }
            ]
        },
        "pages": null,
        "operates": null
    }
```



- 人员标注接口（点击人员标注页面的保存时触发）

```java
1.API路径：http://localhost:8090/api/1/xlbz/person/insert
	后端格式为/api/{recordLog}/xlbz/person/insert，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_INS_PERSON_TAG",
                procedureParamValueList:
                [
                    {fieldName:'P_PERSON_NO_IN', value:''},//人员编号
                    {fieldName:'P_PERSON_TYPE_TAG_IN', value:''},//小类案别
                    {fieldName:'P_PERSON_MEANS_TAG_IN', value:''}//作案手段
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_INSERT_FLAG_OUT_CHAR":"1"
        },
        "pages": null,
        "operates": null
    }
```
