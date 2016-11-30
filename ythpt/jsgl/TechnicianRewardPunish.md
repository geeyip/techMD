## 人员获奖、处分情况

## 获奖情况

列表 

```
/api/{recordLog}/jsgl/technician/rp/1/list?techId={techId}
```

* `techId` 技术人员ID 

新增 

```
/api/{recordLog}/jsgl/technician/rp/1/add?techId={techId}
```

* `techId` 技术人员ID 

修改 

```
/api/{recordLog}/jsgl/technician/rp/edit?id={id}
```

* `id` 获奖情况记录ID

删除 

```
/api/{recordLog}/jsgl/technician/rp/delete?id={id}
```

* `id` 获奖情况记录ID

### 处分情况

列表

```
/api/{recordLog}/jsgl/technician/rp/2/list?techId={techId}
```

* `techId` 技术人员ID

新增 

```
/api/{recordLog}/jsgl/technician/rp/2/add?techId={techId}
```

* `techId` 技术人员ID

修改 

```
/api/{recordLog}/jsgl/technician/rp/edit?id={id}
```

* `id` 处分情况记录ID

删除 

```
/api/{recordLog}/jsgl/technician/rp/delete?id={id}
```

* `id` 处分情况记录ID

### 参数定义

* 获奖、处分日期：rpDate

* 奖励、处分名称：rpName

* 奖励、处分事由：rpReason

* 颁奖机关(单位、部门)：rpPublisher

* 证书图片ID：rpPhotoId

* 证书图片Base64：rpPhoto

* 备注：rpRemark

```json
{
 	"rpDate":"2015-01-01",
    "rpName":"123",
    "rpReason":"456",
    "rpPublisher":"789" ,
    "rpPhotoId":"1111111" ,
    "rpRemark":"000"
}
```

