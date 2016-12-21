## 人员管理API文档

### 获得文件路径

#### API路径

```http
api/{recordLog}/jsgl/technician/file_info
```

其中{recordLog}为前端传入，标识是否需要记录操作志,实际路径如"api/0/jsgl/technician/file_info"

#### 请求

```
POST, application/json
```

#### 传入参数格式
```json
fileId:724c7368c884432ea4f300b5a865009e //文件id(不用jsonStr包裹)
```

#### 返回值格式

```json
{
	"flag": 1,
	"totalCount": 0,
	"msg": null,
	"data": "D:\\project2\\ythgzpt-all\\ythgzpt-web\\target\\ythpt\\tmp\\tt.txt",//文件下载路径
	"pages": null,
	"operates": null
}
```