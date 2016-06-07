## 管理维护

### 用户管理

```http
api/system/user/list
```

获取用户数据

### 角色管理



### 模块管理



### 参数管理



### 系统字典

```HTTP
GET	/api/dict/single/{root}
```

* 根据字典代码类型获取单级字典JSON数据
* `root` 字典代码类型，忽略大小写
* 如果查询多级字典，只返回字典级别为1的数据

```HTTP
GET /api/dict/multi/{root}
```

* 根据字典代码类型获取多级字典JSON数据
* `root` 字典代码类型，忽略大小写

```http
GET /api/dict/{root}/{key}
```

* 根据字典代码类型root与字典key查询字典JSON数据
* `root` 字典代码类型，忽略大小写
* `key` 字典代码

```http
GET /api/dict/{root}/keys/{keys}
```

* 根据字典代码类型root与多个逗号分隔的key查询字典JSON数据
* `root` 字典代码类型，忽略大小写
* `keys` 多个英文逗号分隔的key，例：`/api/dict/xzqhdm/keys/330100,440000`

```http
GET /api/dict/{root}/query?queryType={queryType}&queryString={queryString}
```

* 根据查询条件查询字典信息
* `root` 字典代码类型，忽略大小写
* `queryType`字典查询类型  `1-代码 2-拼音 3-中文`
* `queryString`字典查询字符串
* 当queryType=3时，queryString需要`encodeURI`