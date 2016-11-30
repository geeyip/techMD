## 人员（技术、鉴定）资格

## 技术资格

列表 

```
/api/{recordLog}/jsgl/technician/{techId}/qual/1/list
```

* `techId` 技术人员ID 

新增 

```
/api/{recordLog}/jsgl/technician/{techId}/qual/1/add
```

* `techId` 技术人员ID 

修改 

```
/api/{recordLog}/jsgl/technician/qual/{id}/edit
```

* `id` 技术资格记录ID

删除 

```
/api/{recordLog}/jsgl/technician/qual/{id}/delete
```

* `id` 技术资格记录ID

### 鉴定资格

列表

```
/api/{recordLog}/jsgl/technician/{techId}/qual/2/list
```

* `techId` 技术人员ID

新增 

```
/api/{recordLog}/jsgl/technician/{techId}/qual/2/add
```

* `techId` 技术人员ID

修改 

```
/api/{recordLog}/jsgl/technician/qual/{id}/edit
```

* `id` 鉴定资格记录ID

删除 

```
/api/{recordLog}/jsgl/technician/qual/{id}/delete
```

* `id` 鉴定资格记录ID

### 参数定义

* 资格证编号：bookNo


* 取得时间：getTime


* 到期时间：overTime


* 证书(照片ID)：bookPhotoId

* 证书图片Base64：bookPhoto

* 专业：major

```json
{
"bookNo":"123456",
"getTime":"2012-12-12",
"overTime":"2013-12-11",
"bookPhotoId":"ea5a7546f4b94149a70bc86ece246bc9",
“bookPhoto": "",
"major":"心理学"
}
```

