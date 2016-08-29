## 短信平台API文档

### 发送短信接口

#### API路径

```http
api/{recordLog}/jsgl/note/note_send
```

其中{recordLog}为前端传入，标识是否需要记录操作志,实际路径如"api/0/jsgl/note/note_send"

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
  "ryInfo": "bfed55b9feb3420e8a8028a26636c2e9", //接收消息人员,数据为技术人员id,多个用逗号隔开
  "groupInfo": "7303ef7b57cb4008bbc32e7eb7e47675bfed55b9feb3420e8a8028a26636c2e9", //群发接收消息人员,数据为群组id+技术人员id,
  多个用逗号隔开
  "content": "", //消息内容
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":0,"msg":null,"data":null,"pages":null,"operates":null}
```