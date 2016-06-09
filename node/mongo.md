## mongoDB

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

