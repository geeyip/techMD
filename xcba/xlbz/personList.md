## 人员信息标注API文档

* 人员信息标注查询接口（点击参数管理时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/person/list
	后端格式为/api/{recordLog}/xlbz/person/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_PERSON_ALL_INFO",
                pcdParamValList:
                [
                    {fName:'P_VC_PERSON_NO_IN', fVal:''},//人员编号
                    {fName:'P_D_CREATE_TIME_MIN_IN', fVal:'2016-11-11 11:11:11'},//录入日期开始
                    {fName:'P_D_CREATE_TIME_MAX_IN', fVal:''},//录入日期结束
                    {fName:'P_VC_TAG_P_CASE_TYPE_IN', fVal:''},//小类案别
                    {fName:'P_VC_PERSON_TYPE_IN', fVal:''},//人员类别 0：犯罪；1：违法
                    {fName:'P_D_CAPTURE_TIME_MIN_IN', fVal:''},//抓获日期开始
                    {fName:'P_D_CAPTURE_TIME_MAX_IN', fVal:''},//抓获日期结束
                    {fName:'P_VC_CREATE_UNIT_IN', fVal:''},//管辖单位
                    {fName:'P_N_RECORD_ORDER', fVal:''},//取值开始
                    {fName:'P_N_RECORD_COUNT', fVal:''}//取值截止
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
                "personno": "",//人员编号
                "unit": "2016-11-11 11:11:11",//抓获单位
                "area": "",//发案区划
                "time": "",//抓获日期
                "ptype": "",//人员类别
                "name": "",//姓名
                "cardno": "",//身份证号
                "household": "",//户籍地详址
                "casekind": "",//案件类别
                "casekind2": "",//案件类别1
                "tagckind": "",//小类案别
                "tagmeans": "",//作案手段
                "flag": "",//待标注、已标注
                "order": ""//排序
            },
            {
                "personno": "",//人员编号
                "unit": "2016-11-11 11:11:11",//抓获单位
                "area": "",//发案区划
                "time": "",//抓获日期
                "ptype": "",//人员类别
                "name": "",//姓名
                "cardno": "",//身份证号
                "household": "",//户籍地详址
                "casekind": "",//案件类别
                "casekind2": "",//案件类别1
                "tagckind": "",//小类案别
                "tagmeans": "",//作案手段
                "flag": "",//待标注、已标注
                "order": ""//排序
            }
        ],
        "pages": null,
        "operates": null
    }
```



- 人员抽查接口

```java
1.API路径：http://localhost:8090/api/1/xlbz/person/spot_check
	后端格式为/api/{recordLog}/xlbz/person/spot_check，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_PERSON_CONTENT",
                pcdParamValList:
                [
                    {fName:'P_PERSON_NO_IN', fVal:'R3301835100002016080838'}//人员编号
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":
        [
            {
                "content": "test1"//抽查内容
            }
        ],
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
	            pcdName:"SP_TAG_API_SEL_PERSON_INFO",
                pcdParamValList:
                [
                    {fName:'P_PERSON_NO_IN', fVal:'R3301835100002016080838'}//人员编号
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":
        [
            {
                "personno": "",//人员编号
                "sex": "",//性别
                "name": "",//姓名
                "cardno": "",//身份证号
                "detail": "",//户籍地
                "time": "",//抓获时间
                "tagckind": "",//小类案别
                "tagmeans": "",//作案手段
                "detail": ""//违法犯罪情况
            }
        ],
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
	            pcdName:"SP_TAG_API_INS_PERSON_TAG",
                pcdParamValList:
                [
                    {fName:'P_PERSON_NO_IN', fVal:'R3301835100002016080838'},//人员编号
                    {fName:'P_PERSON_TYPE_TAG_IN', fVal:''},//小类案别
                    {fName:'P_PERSON_MEANS_TAG_IN', fVal:''}//作案手段
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data": "1",
        "pages": null,
        "operates": null
    }
```
