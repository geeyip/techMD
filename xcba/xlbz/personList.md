## 人员信息标注API文档

* 人员信息标注查询接口（点击参数管理时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/person/list
	后端格式为/api/{recordLog}/xlbz/person/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_PERSON_ALL_INFO",
                pcdParamValMap:
                {
                    'pno':'',//人员编号
                    'crttmmin':'',//录入日期开始
                    'crttmmax':'',//录入日期结束
                    'pcstype':'',//小类案别
                    'ptype':'',//人员类别 0：犯罪；1：违法
                    'cptmmin':'',//抓获日期开始
                    'cptmax':'',//抓获日期结束
                    'crtunit':'',//管辖单位
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
                "personno": "",//人员编号
                "unit": "",//抓获单位
                "unitname": "",//抓获单位中文
                "area": "",//发案区划
                "areaname": "",//发案区划中文
                "time": "",//抓获日期
                "ptype": "",//人员类别
                "name": "",//姓名
                "cardno": "",//身份证号
                "household": "",//户籍地详址
                "cridetail": "",//犯罪情况
                "casekind": "",//案件类别
                "kindname": "",//案件类别中文
                "casekind2": "",//案件类别1
                "kindname2": "",//案件类别1中文
                "tagckind": "",//小类案别
                "tagcname": "",//小类案别中文
                "tagmeans": "",//作案手段
                "tagmname": "",//作案手段
                "flag": "",//待标注、已标注
                "order": ""//排序
            },
            {
                "personno": "",//人员编号
                "unit": "",//抓获单位
                "unitname": "",//抓获单位中文
                "area": "",//发案区划
                "areaname": "",//发案区划中文
                "time": "",//抓获日期
                "ptype": "",//人员类别
                "name": "",//姓名
                "cardno": "",//身份证号
                "household": "",//户籍地详址
                "cridetail": "",//犯罪情况
                "casekind": "",//案件类别
                "kindname": "",//案件类别中文
                "casekind2": "",//案件类别1
                "kindname2": "",//案件类别1中文
                "tagckind": "",//小类案别
                "tagcname": "",//小类案别中文
                "tagmeans": "",//作案手段
                "tagmname": "",//作案手段
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
                pcdParamValMap:
                {
                    'pno':'R3301835100002016080838'//人员编号
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
                "content": "test1"//抽查内容
            }
        ],
        "pages": null,
        "operates": null
    }
```



- 人员抽查更新接口

```java
1.API路径：http://localhost:8090/api/1/xlbz/person/check_insert
	后端格式为/api/{recordLog}/xlbz/person/check_insert，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_INS_PERSON_CONTENT",
                pcdParamValMap:
                {
                    'pno':'R3301835100002016080838',//人员编号
                    'pcontent':'2333',//内容
                    'crtunit':'330183'//单位
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



- 人员标注查询接口（点击人员信息标注进入人员标注页面时触发）

```java
1.API路径：http://localhost:8090/api/0/xlbz/person/info
	后端格式为/api/{recordLog}/xlbz/person/info，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_PERSON_INFO",
                pcdParamValMap:
                {
                    'pno':'R3301835100002016080838'//人员编号
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
                "personno": "",//人员编号
                "sex": "",//性别
                "sexname": "",//性别中文
                "name": "",//姓名
                "cardno": "",//身份证号
                "detail": "",//户籍地
                "time": "",//抓获时间
                "tagckind": "",//小类案别
                "kindname": "",//小类案别
                "tagmeans": "",//作案手段
                "meanname": "",//作案手段
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
                pcdParamValMap:
                {
                    'pno':'R3301835100002016080838',//人员编号
                    'ptype':'',//小类案别
                    'pmeans':''//作案手段
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
