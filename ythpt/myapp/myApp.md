# 我的应用API文档

* 我的应用页面查询接口

```java
1.API路径：
2.请求:POST ,application/json
3.传入参数格式：
    jsonStr:{"userid":"8af67d6247aa82060147aa8206c40000"}   //传入的用户名id
4.返回值格式：
    {
    "flag": 1,
    "totalCount": 1,
    "msg": null,
    "data":{
                "appTypes":[
                    {cName:'信息采集',eName:'info-collection'},  //cName:该类的中文名（总共四个大类）
                    {cName:'现场勘验',eName:'xianchang-ky'},     //eName:该类的英文名   
                    {cName:'物证管理',eName:'wzheng-mng'},
                    {cName:'检验鉴定',eName:'jianyi-jianding'}
                ],
                "allApps"：[
                    {"appCName":"平板导入",                //该app的英文名字
                     "appDesc":"对接现勘系统，一站式痕迹物证信息录入，快速关联案件",          //该app的描述
                     "appIcon":"icon-building",           //图标iconfont的名字
                     "appClass":"sdfsdf",                 //app背景色的class
                     "appEname":"padImport",              //例:该app的英文名（代表该app的唯一id表示） 该名字+Handle表示该app的执行函数（例:padImportHandle表示平板导入app的执行函数）
                     "myappsAdded":1,                     //1：表示已添加到我的应用  0:表示没有添加到我的应用
                     "fstpageAdded":0,                    //1：表示已添加到首页      0:表示没有添加到首页
                     "appType":"info-collection"          //表示这个应用属于哪个类 （对应上面的appTypes中的eName）
                    },
                    {"appCName":"现场勘验",
                     "appDesc":"对接现勘系统，一站式痕迹物证信息录入，快速关联案件",
                     "appIcon":"icon-building",pad
                     "appClass":"sdfsdf",
                     "appEname":"stationImportHandle",
                     "myappsAdded":1,
                     "fstpageAdded":1,
                     "appType":"xianchang-ky"
                    }
                    //......
                ]
        }
```



* 页面修改保存接口

```java
1.API路径：
2.请求:POST ,application/json
3.传入参数格式：
    jsonStr:[
        {"appEname":"padImport"，"myappsAdded":0,"fstpageAdded":0},        //appEname：传入后台的修改的app的名字   
        {"appEname":"stationImport"，"myappsAdded":1}                     //myappsAdded: 表示修改后的我的应用 1：表示添加 0：表示不添加 （没有表示原来就已经添加或没有添加，但是没有修改该）
        //.......                                                        //fstpageAdded: 表示修改后的首页的应用 1：表示添加 0：表示不添加（没有表示原来就已经添加或没有添加，但是没有修改该）
    ]
4.返回值格式:
    {"flag":1,msg:'返回成功'}   //flag表示是否返回成功 1：表示成功 0：表示不成功
                                //msg表示返回的描述   返回成功或失败
```

