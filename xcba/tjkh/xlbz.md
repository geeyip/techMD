## 小类标注考核API文档

* 标注时效报表查询接口（点击案件类别时触发）

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/xlbz_sx
	后端格式为/api/{recordLog}/tjkh/xlbz/xlbz_sx，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_TIME_LIMIT",
                pcdParamValMap:{'mintime':'', 'maxtime':''}//统计开始时间,统计结束时间
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data":
        [
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "cttlnum": "",//案件应标数
                "ctagnum": "",//案件已标数
                "cratio": "",//案件标注率
                "cscore": "",//案件得分
                "pttlnum": "",//人员应标数
                "ptagnum": "",//人员已标数
                "pratio": "",//人员标注率
                "pscore": "",//人员得分
                "ttlscore": ""//总得分
            },
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "cttlnum": "",//案件应标数
                "ctagnum": "",//案件已标数
                "cratio": "",//案件标注率
                "cscore": "",//案件得分
                "pttlnum": "",//人员应标数
                "ptagnum": "",//人员已标数
                "pratio": "",//人员标注率
                "pscore": "",//人员得分
                "ttlscore": ""//总得分
            }
        ],
        "pages": null,
        "operates": null
    }
```

* 标注时效报表质量查询接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/sx_bzzl
	后端格式为/api/{recordLog}/tjkh/xlbz/sx_bzzl，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_EXPLAIN",
                pcdParamValMap:
                {
                    'rptname':'SP_TAG_API_SEL_REP_TIME_LIMIT',//对应报表的存储过程名称
                    'time':'2016-09-20'//查询截止时间
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
                "content": ""//质量内容
            }
        ],
        "pages": null,
        "operates": null
    }
```

* 标注率报表查询接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/xlbz_lv
	后端格式为/api/{recordLog}/tjkh/xlbz/xlbz_lv，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_TAG",
                pcdParamValMap:{'mintime':'', 'maxtime':''}//统计开始时间,统计结束时间
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data":
        [
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "cttlnum": "",//案件应标数
                "ctagnum": "",//案件已标数
                "cratio": "",//案件标注率
                "cscore": "",//案件得分
                "pttlnum": "",//人员应标数
                "ptagnum": "",//人员已标数
                "pratio": "",//人员标注率
                "pscore": "",//人员得分
                "ttlscore": ""//总得分
            },
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "cttlnum": "",//案件应标数
                "ctagnum": "",//案件已标数
                "cratio": "",//案件标注率
                "cscore": "",//案件得分
                "pttlnum": "",//人员应标数
                "ptagnum": "",//人员已标数
                "pratio": "",//人员标注率
                "pscore": "",//人员得分
                "ttlscore": ""//总得分
            }
        ],
        "pages": null,
        "operates": null
    }
```

* 标注率报表质量查询接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/lv_bzzl
	后端格式为/api/{recordLog}/tjkh/xlbz/lv_bzzl，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_EXPLAIN",
                pcdParamValMap:
                {
                    'rptname':'SP_TAG_API_SEL_REP_TAG',//对应报表的存储过程名称
                    'time':'2016-09-20'//查询截止时间
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
                "content": ""//质量内容
            }
        ],
        "pages": null,
        "operates": null
    }
```

* 标注质量报表查询接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/xlbz_zl
	后端格式为/api/{recordLog}/tjkh/xlbz/xlbz_zl，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_CHECK",
                pcdParamValMap:{'mintime':'', 'maxtime':''}//统计开始时间,统计结束时间
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data":
        [
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "ctagnum": "",//案件抽查数
                "cscore": "",//案件得分
                "ptagnum": "",//人员应标数
                "pscore": "",//人员得分
                "ttlscore": ""//总得分
            },
            {
                "time": "2016-11-11",//日期
                "unit": "",//单位
                "ctagnum": "",//案件抽查数
                "cscore": "",//案件得分
                "ptagnum": "",//人员应标数
                "pscore": "",//人员得分
                "ttlscore": ""//总得分
            }
        ],
        "pages": null,
        "operates": null
    }
```

* 标注质量报表质量查询接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/zl_bzzl
	后端格式为/api/{recordLog}/tjkh/xlbz/zl_bzzl，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_REP_EXPLAIN",
                pcdParamValMap:
                {
                    'rptname':'SP_TAG_API_SEL_REP_CHECK',//对应报表的存储过程名称
                    'time':'2016-09-20'//查询截止时间
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
                "content": ""//质量内容
            }
        ],
        "pages": null,
        "operates": null
    }
```

* 标注质量报表质量更新接口

```java
1.API路径：http://localhost:8090/api/1/tjkh/xlbz/zl_update
	后端格式为/api/{recordLog}/tjkh/xlbz/zl_update，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_UPD_REP_EXPLAIN",
                pcdParamValMap:
                {
                    'rptname':'SP_TAG_API_SEL_REP_CHECK',//对应报表的存储过程名称
                    'time':'2016-09-20',//查询截止时间
                    'content':'test'//更新内容
                }
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":"1",
        "pages": null,
        "operates": null
    }
```

* 小类标注考核Excel导出接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/xlbzkhExcel
	后端格式为/api/{recordLog}/tjkh/xlbz/xlbzkhExcel，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：GET, application/json
3.传入参数格式：
	jsonStr:{}
4.返回值格式
	{}
```

* 小类标注考核Word导出接口

```java
1.API路径：http://localhost:8090/api/0/tjkh/xlbz/xlbzkhWord
	后端格式为/api/{recordLog}/tjkh/xlbz/xlbzkhWord，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：GET, application/json
3.传入参数格式：
	jsonStr:{}
4.返回值格式
	{}
```

