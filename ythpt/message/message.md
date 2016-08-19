## 系统消息API文档

### 发消息接口

点击查询按钮时触发

#### API路径

```http
http://localhost:8090/api/1/system/message/sendMessage
```

后端格式为`/api/{recordLog}/system/message/sendMessage`，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "subject": "", //消息标题
  "content": "", //消息内容
  "tslb": "", //消息类型
  "receiverList":[   //消息接收人数组
	  {
			'senderName':'',//发送人姓名
			'senderId':'',//发送人ID
			'senderUnit':'',//发送方所属单位
			'receiverId':'',//接收人ID
			'receiverName':'',//接收人姓名
		}
  ]
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```