## 案件信息标注API文档

* 案件信息标注查询接口（点击参数管理时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/case/list
	后端格式为/api/{recordLog}/xlbz/case/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_CASE_ALL_INFO",
                pcdParamValMap:
                {
                    'cno':'',//案件编号
                    'crttmmin':'',//录入日期开始
                    'crttmmax':'',//录入日期结束
                    'ctype':'',//小类案别
                    'cbrief':'',//简要案情
                    'hptmmin':'',//案发时间开始
                    'hptmmax':'',//案发时间结束
                    'crtunit':'',//管辖单位
                    'usurflg':'',//是否侵财 1:侵财；0：非侵财
                    'cstatus':'',//案件状态
                    'rcdorder':'',//取值开始
                    'rcdcount':''//取值截止
                }
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
                "areaname": "",//发案区划中文
                "address": "",//案发地点
                "summary": "",//简要案情
                "kind": "",//案件类别
                "kindname": "",//案件类别中文
                "status": "",//案件状态
                "stname": "",//案件状态中文
                "unit": "",//录入单位
                "unitname": "",//录入单位中文
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
                "areaname": "",//发案区划中文
                "address": "",//案发地点
                "summary": "",//简要案情
                "kind": "",//案件类别
                "kindname": "",//案件类别中文
                "status": "",//案件状态
                "stname": "",//案件状态中文
                "unit": "",//录入单位
                "unitname": "",//录入单位中文
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
	            pcdName:"SP_TAG_API_SEL_CASE_CONTENT",
                pcdParamValMap:
                {
                    'cno':'A3301855500002016090001'//案件编号
                }
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
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



- 案件抽查更新接口

```java
1.API路径：http://localhost:8090/api/1/xlbz/case/check_insert
	后端格式为/api/{recordLog}/xlbz/case/check_insert，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_INS_CASE_CONTENT",
                pcdParamValMap:
                {
                    'cno':'A3301855500002016090001',//案件编号
                    'ccontent':'6666',//内容
                    'crtunit':'330185'//单位
                }
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



- 案件标注查询接口（点击案件信息标注进入案件标注页面时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/case/info
	后端格式为/api/{recordLog}/xlbz/case/info，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_CASE_INFO",
                pcdParamValMap:
                {
                    'cno':'A3301855500002016090001'//案件编号
                }
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":
        [
            {
                "caseno": "",//案件编号
                "happentime": "",//案发时间
                "address": "",//案发地点
                "unit": "",//选择单位
                "unitname": "",//选择单位中文
                "solvetime": "",//破案时间
                "status": "",//案件状态
                "stname": "",//案件状态中文
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
	            pcdName:"SP_TAG_API_INS_CASE_TAG",
                pcdParamValMap:
                {
                    'cno':'A3301855500002016090001',//案件编号
                    'ctype':'',//小类案别
                    'cmeans':''//作案手段
                }
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
