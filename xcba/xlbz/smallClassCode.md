## 小类标注代码API文档

* 小类标注代码查询所有大类接口

```java
1.API路径：http://api/0/xlbz/xldm/list
	后端格式为/api/{recordLog}/xlbz/xldm/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_BIG_TYPE"
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
                    "key":"4000",//案件类别代码
                    "value":"窃取手段",//案件类别中文
                    "type":"A"//案件类别类型,A-大类,B-小类,C-手段
                },
                {
                    "key":"3000",//案件类别代码
                    "value":"暴力胁迫手段",//案件类别中文
                    "type":"A"//案件类别类型,A-大类,B-小类,C-手段
                }
            ]
        },
        "pages": null,
        "operates": null
    }
```


* 小类标注代码分层查询案件类别接口

```java
1.API路径：http://api/0/xlbz/xldm/layeredList
	后端格式为/api/{recordLog}/xlbz/xldm/layeredList，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_PART_CASE_KIND",
	             procedureParamValueList:
                [
                    {fieldName:'P_DICT_KEY_IN', value:'4000'}//父级案件类别
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_PART_KIND_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "key":"4100",//案件类别代码
                    "value":"破锁开锁"//案件类别中文
                },
                {
                    "key":"4200",//案件类别代码
                    "value":"破盗金柜"//案件类别中文
                }
            ]
        },
        "pages": null,
        "operates": null
    }
```


* 小类标注代码新增接口

```java
1.API路径：http://api/1/xlbz/xldm/add
	后端格式为/api/{recordLog}/xlbz/xldm/add，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_INS_TAG_CASE_KIND",
                procedureParamValueList:
                [
                    {fieldName:'P_DICT_TYPE1_IN', value:'A'},//父
                    {fieldName:'P_DICT_TYPE2_IN', value:'B'},//子
                    {fieldName:'P_DICT_KEY1_IN', value:'4200'},//选中的类别代码
                    {fieldName:'P_DICT_VALUE2_IN', value:''}//新增名称
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_INSERT_FLAG_OUT_CHAR":"1"//新增结果,1:成功,0:失败
        },
        "pages": null,
        "operates": null
    }
```


* 小类标注代码修改接口

```java
1.API路径：http://api/1/xlbz/xldm/edit
	后端格式为/api/{recordLog}/xlbz/xldm/edit，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_UPD_TAG_CASE_KIND",
                procedureParamValueList:
                [
                    {fieldName:'P_DICT_KEY1_IN', value:'4200'},//选中类别代码
                    {fieldName:'P_DICT_VALUE2_IN', value:'杀人越货'}//修改后名称
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_UPDATE_FLAG_OUT_CHAR":"1"//修改结果,1:成功,0:失败
        },
        "pages": null,
        "operates": null
    }
```

