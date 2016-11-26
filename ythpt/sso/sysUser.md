##统一认证系统用户管理

### 页面查询接口(初始进入模块)

点击查询按钮时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/system/user/list_sso
```

后端格式为`/api/{recordLog}/system/user/list_sso`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
    {
        "queryCondition":
            {
                "userName":"",
                "account":""
            },
        "begin":1,
        "end":200
    }
```


#### 返回值格式

```json
    {
        "flag":1,
        "totalCount":1,
        "msg":null,
        "data":[
            {
                "status":0,
                "createAccount":null,
                "createTime":0,
                "lastModifyTime":0,
                "lastModifyAccount":null,
                "lastTerminal":null,
                "lastSys":null,
                "indexNum":0,
                "userId":"90132ed4a7b94dd1a08b7ffcc50962ba",
                "userName":"晏海先",
                "sex":0,
                "cid":"420581198106011016",
                "isPolice":0,
                "policeId":"220221",
                "contact":null,
                "avatar":null,
                "post":null,
                "postName":null,
                "birth":0,
                "poli":null,
                "poliName":null,
                "phone":null,
                "fax":null,
                "address":null,
                "zipcode":null,
                "province":null,
                "provinceName":null,
                "city":null,
                "cityName":null,
                "county":null,
                "countyName":null,
                "extStr1":null,
                "extStr2":null,
                "extStr3":null,
                "account":"晏海先",
                "pass":"92894219EF3E7B6D752F058D31C5166C",
                "userType":0,
                "activeStatus":1,
                "orgId":"f1c0f6413e764b559bb215ded418a218",
                "orgName":"厦门市公安局思明分局刑事侦查大队",
                "orgCode":"350203240000",
                "orgType":1,
                "roleName":"质量管理员"
             }
        ],
        "pages":null,
        "operates":null
    }
````

### 用户信息查看接口

点击用户账号时触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/system/user/view_sso
```

后端格式为`/api/{recordLog}/system/user/view_sso`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
    {
        "account":"晏海先"
    }
```
#### 返回值格式

```json
    {
        "flag":1,
        "totalCount":0,
        "msg":null,
        "data":
            {
                "status":0,
                "createAccount":null,
                "createTime":0,
                "lastModifyTime":0,
                "lastModifyAccount":null,
                "lastTerminal":null,
                "lastSys":null,
                "indexNum":0,
                "userId":"90132ed4a7b94dd1a08b7ffcc50962ba",
                "userName":"晏海先",
                "sex":0,
                "cid":"420581198106011016",
                "isPolice":0,
                "policeId":"220221",
                "contact":null,
                "avatar":"",
                "post":null,
                "postName":null,
                "birth":0,
                "poli":null,
                "poliName":null,
                "phone":null,
                "fax":null,
                "address":null,
                "zipcode":null,
                "province":null,
                "provinceName":null,
                "city":null,
                "cityName":null,
                "county":null,
                "countyName":null,
                "extStr1":null,
                "extStr2":null,
                "extStr3":null,
                "account":"晏海先",
                "pass":"92894219EF3E7B6D752F058D31C5166C",
                "userType":0,
                "activeStatus":1,
                "orgId":"f1c0f6413e764b559bb215ded418a218",
                "orgName":"厦门市公安局思明分局刑事侦查大队",
                "orgCode":"350203240000",
                "orgType":1,
                "roleName":"质量管理员"
            },
        "pages":null,
        "operates":null
    }
```

### 进入用户信息修改接口

点击修改按钮时触发

#### API路径

```http
http://localhost:8081/>ythpt/api/1/system/user/_edit_sso
```

后端格式为`/api/{recordLog}/system/user/_edit_sso`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
    {
        "account":"晏海先"
    }
```

#### 返回值格式

```json
    {
        "flag":1,
        "totalCount":1,
        "msg":null,
        "data":
            {
                "userRoleIds":"151e19acae5744caa1b33e92598af53d,15ac0766ef4640719f0eacdb73ed0ffd,30a22546c0e242e980d31f5c751cd565",
                "allRoleList":[
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"15ac0766ef4640719f0eacdb73ed0ffd","roleName":"质量管理员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"30a22546c0e242e980d31f5c751cd565","roleName":"质量负责人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"bb762de470d14cdf898cdc947cfccd35","roleName":"质管办负责人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"151e19acae5744caa1b33e92598af53d","roleName":"系统管理员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"fe8b9583af614c0c805c8b3a7f8bdc99","roleName":"物证库管理员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"aaa68a43960a4357ae47a1b1cd885732","roleName":"委托送检人员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"2fde70d5ba2e4b2a82984271c3aaa3b4","roleName":"授权签字人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"9661e4d99d594e7782c8639ab844a2dc","roleName":"试剂耗材管理员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"7803238b3710405daacc6a800640cab6","roleName":"实验室负责人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"f92d4e45410547c0a30b8194f7aae473","roleName":"设备管理员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"1853a1adcd9c42fb809e4c5a503464ec","roleName":"鉴定受理人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"11e20a558bef47088e9cf1846497680e","roleName":"鉴定室主任","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"faa3361ffe22453dbfee8f5f1e4577a3","roleName":"检验人员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"e50ab89bb2d548e58d1399cb829eb173","roleName":"技术负责人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"978afafac159401692de6bcf60040f26","roleName":"管理人员","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"efa63548d3024b6ab5ad8e9ac51ee7c6","roleName":"访客","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"11c1c54720e04024b641f25fd843c81c","roleName":"档案保管人","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"UAOP","createTime":1471245322716,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"roleId":"f51dbf1d7aa8464b87880d17bd330210","roleName":"super","superId":"1","type":1,"note":null,"systemId":null,"activeStatus":1},
                    {"status":0,"createAccount":"unkown","createTime":1479283146175,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":"0.0.0.0","lastSys":"unkown","indexNum":0,"roleId":"146cee1b01894228b8527904f2ff8d2b","roleName":"测试人员test","superId":"0","type":1,"note":"测试人员test","systemId":null,"activeStatus":1}
                ],
                "user":{"status":0,"createAccount":null,"createTime":0,"lastModifyTime":0,"lastModifyAccount":null,"lastTerminal":null,"lastSys":null,"indexNum":0,"userId":"6b41c49355d240e99985fa9fc3502740","userName":"琚发明","sex":0,"cid":"45272819850806001X","isPolice":0,"policeId":"103158","contact":null,"avatar":"","post":null,"postName":null,"birth":0,"poli":null,"poliName":null,"phone":null,"fax":null,"address":null,"zipcode":null,"province":null,"provinceName":null,"city":null,"cityName":null,"county":null,"countyName":null,"extStr1":null,"extStr2":null,"extStr3":null,"account":"琚发明","pass":"CF814721358D09942B255746542AD2A4","userType":0,"activeStatus":1,"orgId":"aa3335942a8848799ebc6346872becd9","orgName":"福州市公安局瀛洲派出所","orgCode":"350103700000","orgType":1,"roleName":"系统管理员"}
            },
        "pages":null,
        "operates":null
    }
```

### 保存修改的用户信息接口

点击用户修改页面保存按钮触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/system/user/edit_sso
```

后端格式为`/api/{recordLog}/system/user/edit_sso`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
   {
        "remark":"",
        "activeStatus":"1",
        "pass":"",
        "userId":"6b41c49355d240e99985fa9fc3502740",
        "userName":"琚发明",
        "account":"琚发明",
        "roleId":"151e19acae5744caa1b33e92598af53d,15ac0766ef4640719f0eacdb73ed0ffd"
   }
```
#### 返回值格式

```json
    {
        "flag":1,
        "totalCount":0,
        "msg":null,
        "data":null,
        "pages":null,
        "operates":null
    }
```

### 用户删除接口

点击删除按钮触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/system/user/delete_sso
```

后端格式为`/api/{recordLog}/system/user/delete_sso`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
GET, application/json
```

#### 传入参数格式
```
    userId:1ca6565c36d14427bd67d606140771bb
```
#### 返回值格式

```json
    {
        "flag":1,
        "totalCount":0,
        "msg":null,
        "data":null,
        "pages":null,
        "operates":null
    }
```

### 用户新增接口

点击新增按钮触发

#### API路径

```http
http://localhost:8081/ythpt/api/1/system/user/add_sso
```

后端格式为`/api/{recordLog}/system/user/add_sso`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
   {
        "remark":"",
        "activeStatus":"1",
        "pass":"test1",
        "userId":"174e80c0fc424cac874e71665ccc9eb3",
        "userName":"阙培崇",
        "account":"test1"
   }
```



#### 返回值格式

```json
    {
        "flag":1,
        "totalCount":0,
        "msg":null,
        "data":null,
        "pages":null,
        "operates":null
    }
```
