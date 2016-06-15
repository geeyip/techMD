## 管理维护

### 用户管理

```http
 /api/{recordLog}/system/user
```

* 用户管理通用路径前缀
* `recordLog` 记录日志标志，填写1时表示加入操作日志，如`api/1/system/user/list`

```http
POST /api/{recordLog}/system/user/list
```

* 获取登录用户列表

```http
POST /api/{recordLog}/system/user/delete
```

* 删除登录用户

```http
GET /api/{recordLog}/system/user/view
```

* 查看登录用户

```http
GET /api/{recordLog}/system/user/_edit
```

* 进入用户管理修改

```http
POST /api/{recordLog}/system/user/edit
```

* 用户管理修改

```http
POST /api/{recordLog}/system/user/add
```

* 用户管理新增

```http
POST /api/{recordLog}/system/user/password
```

* 修改密码



### 角色管理

```http
 /api/{recordLog}/system/role
```

* 角色管理通用路径前缀
* `recordLog` 记录日志标志，填写1时表示加入操作日志，如`api/1/system/role/list`

```http
POST /api/{recordLog}/system/role/list
```

* 获得角色管理列表

```http
POST /api/{recordLog}/system/role/delete
```

* 删除角色

```http
POST /api/{recordLog}/system/role/add
```

* 新增角色

```http
GET /api/{recordLog}/system/role/_edit
```

* 进入角色修改

```http
POST /api/{recordLog}/system/role/edit
```

* 修改角色信息

```http
GET /api/{recordLog}/system/role/_user
```

* 进入用户分配

```http
GET /api/{recordLog}/system/role/remove_user
```

* 角色移除用户

```http
GET /api/{recordLog}/system/role/add_user
```

* 角色新增用户

```http
GET /api/{recordLog}/system/role/_permission
```

* 进入角色授权

```http
GET /api/{recordLog}/system/role/permission
```

* 修改角色授权


### 模块管理

```http
GET /api/{recordLog}/system/module
```

* 模块管理通用路径前缀
* `recordLog` 记录日志标志，填写1时表示加入操作日志，如`api/1/system/module/view`

* 查看模块信息
```http
GET /api/{recordLog}/system/module/view
```

* 新增模块
```http
POST /api/{recordLog}/system/module/add
```

* 删除模块
```http
GET /api/{recordLog}/system/module/delete
```

* 更新模块信息
```http
POST /api/{recordLog}/system/module/update
```


### 参数管理

```http
GET /api/{recordLog}/system/param
```

* 参数管理通用路径前缀
* `recordLog` 记录日志标志，填写1时表示加入操作日志，如`api/1/system/param/add`

* 新增系统参数

```http
POST /api/{recordLog}/system/param/add
```

* 修改系统参数
```http
POST api/{recordLog}/system/param/edit
```


### 系统登录日志

```http
POST /api/{recordLog}/system/login/log
```

* 系统登录日志通用路径前缀
* `recordLog` 记录日志标志，填写1时表示加入操作日志，如`api/1/system/login/log`

* 查询登录用户日志
```http
POST /api/{recordLog}/system/login/log
```


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
