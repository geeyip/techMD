## 小类标注代码API文档

* 小类标注代码查询列表接口

```java
1.API路径：http://api/0/xlbz/xldm/list
	后端格式为/api/{recordLog}/xlbz/xldm/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_SEL_CASE_KIND",
	            procedureParamValueList:
                [
                    {fieldName:'P_VC_FLAG', fieldValue:'1'}//1:大类-小类-手段
                ]
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": 1,
        "msg": null,
        "data": {
            "P_RESULT_OUT_OUT_SYS_REFCURSOR":
            [
                {
                    "VC_KEY1":"4000",//大类代码
                    "VC_NAME1":"窃取手段",//中文名
                    "VC_KEY2":"4100"//小类代码
                    "VC_NAME2":"破锁开锁",//中文名
                    "VC_KEY3":"4101",//手段代码
                    "VC_NAME3":"硬物击锁"//中文名
                },
                {
                    "VC_KEY1":"4000",
                    "VC_NAME1":"窃取手段",
                    "VC_KEY2":"4100"
                    "VC_NAME2":"破锁开锁",
                    "VC_KEY3":"4101",//
                    "VC_NAME3":"硬物击锁"
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
//对应下方4个请求参数
//{'','A','','新增大类名称'}
//{'A','B','选中的大类的代码','新增小类名称'}
//{'A','C','选中的大类代码','新增手段名称'}
//{'B','C','选中的小类代码','新增手段名称'}
3.传入参数格式：
	jsonStr:{
	            procedureName:"SP_TAG_API_INS_TAG_CASE_KIND",
                procedureParamValueList:
                [
                    {fieldName:'P_DICT_TYPE1_IN', fieldValue:'A'},//父
                    {fieldName:'P_DICT_TYPE2_IN', fieldValue:'B'},//子
                    {fieldName:'P_DICT_KEY1_IN', fieldValue:'4200'},//选中的类别代码
                    {fieldName:'P_DICT_VALUE2_IN', fieldValue:''}//新增名称
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
                    {fieldName:'P_DICT_KEY1_IN', fieldValue:'4200'},//选中类别代码
                    {fieldName:'P_DICT_VALUE2_IN', fieldValue:'杀人越货'}//修改后名称
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

