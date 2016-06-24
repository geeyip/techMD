## mongoDB 安装与启动

### 安装

* 安装步骤略


* 注意安装路径**不要有空格**

 ### 启动

```shell
mongod --dbpath D:\data --logpath D:\logs --logappend --install
```

* 在安装目录下找到`bin`  目录，在`bin`目录下使用命令窗口执行上面命令
* `dbpath` 和 `logpath`后面的文件夹绝对路径要存在
* `logappend`  参数表示日志只在一个文件中追加
* `install` 参数表示安装为windows系统服务，默认服务名为`MongoDB`

### 连接

```shell
mongo
```

* 在安装目录下找到`bin`  目录，在`bin`目录下使用命令窗口执行上面命令,即可连接数据库



## mongoDB 命令

```shell

# 切换或创建数据库
use mydb

# 当前数据库
db

# 查看数据库列表
show dbs

# 删除数据库
db.dropDatabase()

# 创建集合
db.createCollection(name, options)

# 查看集合列表
show collections

# 删除集合
db.mycollection.drop()

# 插入文档
db.mycollection.insert(document)

# 查询文档
db.mycol.find().pretty()
db.mycol.find({"by":"tutorials yiibai"}).pretty()
db.mycol.find({"likes":{$lt:50}}).pretty()
db.mycol.find({"likes":{$lte:50}}).pretty()
db.mycol.find({"likes":{$gt:50}}).pretty()
db.mycol.find({"likes":{$gte:50}}).pretty()
db.mycol.find({"likes":{$ne:50}}).pretty()

# 且查询
db.mycol.find({key1:value1, key2:value2}).pretty()

# 或查询
db.mycol.find(
   {
      $or: [
	     {key1: value1}, {key2:value2}
      ]
   }
).pretty()

# 且或一起查询
db.mycol.find("likes": {$gt:10}, $or: [{"by": "yiibai"}, {"title": "MongoDB Overview"}] }).pretty()

# 更新文档(一个)
db.mycol.update({'title':'MongoDB Overview'},{$set:{'title':'New MongoDB Tutorial'}})

# 更新文档(多个)
db.mycol.update({'title':'MongoDB Overview'},{$set:{'title':'New MongoDB Tutorial'}},{multi:true})

# 删除文档
db.mycol.remove({'title':'MongoDB Overview'})

# 删除集合内所有文档
db.mycol.remove()

# 控制查询文档字段显示
db.mycol.find({},{"title":1,_id:0})

# 控制查询文档条数
db.mycol.find({},{"title":1,_id:0}).limit(2)

# 跳过文档数
db.mycol.find({},{"title":1,_id:0}).limit(1).skip(1)

# 文档排序
db.mycol.find({},{"title":1,_id:0}).sort({"title":-1})

# 创建索引
db.mycol.ensureIndex({"title":1,"description":-1})

```

## update(query, data, upsert, updateAll)

```javascript
db.badperson.update({_id:'112345'}, {name:'aba', age: 12});
```

### $set

修改特定属性

```javascript
db.badperson.update({_id:'112345'}, {$set: {name:'aba', age: 12}});
```

### $unset

移除文档属性

```javascript
db.badperson.update({_id:'112345'}, {$unset: {age: 12}});
```

### $inc

属性值累加

```javascript
db.badperson.update({_id:'112345'}, {$inc: {age: 12}});
```

### $push

数组增加

```javascript
db.badperson.update({_id:'112345'},{$push: {card:'1122'}});
```

### $each

```javascript
db.badperson.update({_id:'112345'},{$push: {card: {$each: ['111','222']}}});
```

### $slice

保持数组固定大小

```javascript
db.badperson.update({_id:'112345'},{$push: {card: {$each: ['111','222'],$slice:-10,$sort:1}}});
```

返回数组固定大小子集

```javascript
db.badperson.find({address:'asdf'},{card: {$slice:-1}})
```

### $addToSet

加入数组并可查重

```javascript
db.badperson.update({_id:'112345'},{$addToSet: {card: {$each: ['111','333']}}});
```

### $pull

移除数据中包好111的元素

```javascript
db.badperson.update({_id:'112345'},{$pull:{card:'111'}})
```



## find(query, column)

### $ne

不等于

```javascript
db.badperson.find({'age':{$ne: 44}});
```

### $lt

小于

```javascript
db.badperson.find({'age':{$lt: 44}});
```

### $lte

小于等于

```javascript
db.badperson.find({'age':{$lte: 44}});
```

### $gt

大于

```javascript
db.badperson.find({'age':{$gt: 44}});
```

### $gte

大于等于

```javascript
db.badperson.find({'age':{$gte: 44}});
```

### $in

值在给定数组中

```javascript
db.badperson.find({'age':{$in: [23,44]}});
```

### $nin

值不在给定数组中

```javascript
db.badperson.find({'age':{$nin: [23,44]}});
```

### $not

结果取反

```javascript
db.badperson.find({'age':{$not: {$nin: [23,44]}}});
```

### $or

查询姓名叫王五或者年龄大于35的人

```javascript
db.badperson.find({$or: [{name:'王五'}, {'age': {$gt: 35}}]});
```

### $and

查询姓名叫王五并且年龄大于30的人

```javascript
db.badperson.find({$and: [{name:'王五'}, {age: {$gt: 30}}]});
```

```javascript
db.badperson.find({name:'王五', age: {$gt: 30}});
```

### $all

数组查询和标量一样

```javascript
db.badperson.find({card: '222'}) //card是数组
```

匹配所有给定值, 

```javascript
db.badperson.find({card: {$all: ['222','333']}}) //card中既有222又有333
```

### $size

查询给定长度的数组

```javascript
db.badperson.find({'card': {$size: 2}})
```

### $elemMatch

数组匹配和内嵌文档查询

```javascript
db.badperson.find({'card': {$elemMatch: {$lt: 33, $gt: 22}});
```

### limit

返回前5条数据

```javascript
db.badperson.find().limit(5);
```

### skip

跳过条数，避免略过大量结果

```javascript
db.badperson.find().limit(5).skip(5);
```

### sort

排序

```javascript
db.badperson.find().limit(5).skip(5).sort({name: -1});
```



