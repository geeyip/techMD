## 小类标注代码API文档

* 小类标注代码查询列表接口

```java
1.API路径：http://localhost:8020/api/0/xlbz/xldm/list
	后端格式为/api/{recordLog}/xlbz/xldm/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_CASE_KIND",
	            pcdParamValMap:
                    {"flag":"1"}//1:大类-小类-手段
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":[
                {
                    "key1":"4000",//大类代码
                    "name1":"窃取手段",//中文名
                    "key2":"4100"//小类代码
                    "name2":"破锁开锁",//中文名
                    "key3":"4101",//手段代码
                    "name3":"硬物击锁"//中文名
                },
                {
                    "key1":"4000",
                    "name1":"窃取手段",
                    "key2":"4100"
                    "name2":"破锁开锁",
                    "key3":"4101",//
                    "name3":"硬物击锁"
                }
            ],
        "pages": null,
        "operates": null
    }
```


* 小类标注代码查询所有大类接口

```java
1.API路径：http://api/0/xlbz/xldm/classList
	后端格式为/api/{recordLog}/xlbz/xldm/classList，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_BIG_TYPE"
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data":
            [
                {"type":"A","key":"501","name":"抢劫"},
                {"type":"A","key":"505","name":"抢夺"}
            ],
        "pages": null,
        "operates": null
    }
```


* 小类标注代码查询分层数据列表接口

```java
1.API路径：http://api/0/xlbz/xldm/layeredList
	后端格式为/api/{recordLog}/xlbz/xldm/layeredList，其中{recordLog}为前端传入，标识是否需要记录操作日志。
2.请求：POST, application/json
3.传入参数格式：
	jsonStr:{
	            pcdName:"SP_TAG_API_SEL_PART_CASE_KIND",
	            pcdParamValMap:
                    {"dictkey":"501"}
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data": [
        .       {"prkey":"501","type":"B","key":"5010100","name":"测试小类"},
                {"prkey":"501","type":"C","key":"5010001","name":"拦路抢劫"}
            ],
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
	            pcdName:"SP_TAG_API_INS_TAG_CASE_KIND",
                pcdParamValMap:
                    {"dicttyp1":"A","dicttyp2":"B","dictkey1":"4200","dictval2":"测试名称"}//父,子,选中的类别代码,新增名称
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data": "1",//新增结果,1:成功,0:失败,
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
	            pcdName:"SP_TAG_API_UPD_TAG_CASE_KIND",
                pcdParamValMap:
                    {"dictkey1":"4200","dictval2":"杀人越货"}//选中类别代码,修改后名称
	        }
4.返回值格式
	{
        "flag": 1,
        "totalCount": -1,
        "msg": null,
        "data": null,
        "pages": null,
        "operates": null
    }
```

