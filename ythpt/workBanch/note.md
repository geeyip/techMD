## 勘验笔录制作API文档

### 勘验笔录制作查询接口

#### API路径

```http
http://localhost:8095/api/0/workbench/kyblzz/list
```

后端格式为`/api/{recordLog}/workbench/kyblzz/list，其中{recordLog}为前端传入，标识是否需要记录操作日志。

#### 请求

```
POST, application/json
```

#### 传入参数格式
**jsonStr:**
```json
{
"begin":1,"end":60,"faqh":"350200000000","ajlb":"050101",
"kysjStart":"2016-06-23","kysjEnd":"2016-06-25",
"investigationNo":"K3502062","kydd":"厦门市","fadd":"湖里区",
"investigatorId":"8a023cd43a8b154e013ad89786032b67","sfzz":"1"
}
```

#### 返回值格式

```json
{"flag":1,"totalCount":1,"msg":null,"data":
[{"dqpSatisfyFlag":null,"fwsytAmount":0,"pmsytAmount":0,"fwzpAmount":0,"gmzpAmount":0,"zdbwzpAmount":0,
"rownum":"1","begin":0,"end":0,"alarmNo":null,"caseNo":null,"receptionNo":null,"caseId":null,"caseType":null,
"casePlace":null,"investigationId":"8a023cd4554c85f701559643f0285a59","investigationNo":"K3502062400002016060208",
"investigator":null,"investigatorId":"8a023cd43a8b154e013ad89786032b67,8a023cd43a8b154e013ad89785f42b61",
"investigationPlace":null,"qualifiedFlag":"已提交","saveFlag":null,"finishFlag":null,"investigationTime":null,
"investigationTimeStart":null,"investigationTimeEnd":null,"evidenceAmount":null,"scenePhotoAmount":null,
"scenePictureAmount":null,"sceneVideoAmount":null,"sceneEvidenceAmount":null,"baseStationAmount":null,"sceneArea":null,
"isToCase":null,"lawId":null,"exposureProcess":null,"director":null,"content":null,
"updatedInvestNoteId":"8a023cd4559650470155965f46ba015a",
"unQualifyReason":null,"reservation01":null,"reservation02":null,"reservation03":null,"reservation04":null,
"reservation05":null,"reservation06":null,"reservation07":null,"reservation08":null,"reservation09":null,
"reservation10":null,"createUser":null,"createUserId":null,"initServerNo":null,"sceneRegionalism":null,"id":null,
"kybh":null,"jqbh":null,"ajbh":"A3502062400002016060159","kysj":"2016-06-23 17:00",
"kydd":"福建省厦门市湖里区林后社63号百佳批发部","ajlb":"入户抢劫案","faqh":null,
"fadd":"福建省厦门市湖里区林后社63号百佳批发部","kyr":"王恩宽、王书龙","xczt":null,"sfyq":null,"dxsl":0,"xxsl":0,
"sfgl":null,"zdjkajl":null,"kysjStart":null,"kysjEnd":null,"kysjDate":"2016-06-23 17:00:00","bhglx":null,"jcxx":0,
"kybl":0,"xct":0,"xczp":0,"hj":0,"dqp":0,"lrr":null,"lrrId":null,"lrsj":null,"sfsc":null,"sfhg":null,"sfzg":null,
"picNum":null,"fasj":null,"type":null,"jyaq":null,"sfrd":null,"znjc":null,"snw":null,"score":null,"lasj":null,
"lasjStart":null,"lasjEnd":null,"ccsl":null,"lsccjg":null,"fasjStart":null,"fasjEnd":null,"lrsjStart":null,
"lrsjEnd":null,"tjsjStart":null,"tjsjEnd":null,"zwtqs":0,"zwtjs":0,"zjtqs":0,"jztqs":0,"zjtjs":0,"dnatqs":0,
"gjtqs":0,"dztqs":0,"sttqs":0,"qdtqs":0,"tstqs":0,"dhtqs":0,"lhtqs":0,"wjtqs":0,"qttqs":0,"dnasjs":0,"tqwps":0,
"dnawsjs":0,"zwwtjs":0,"zjwtjs":0,"qtwztqs":0,"sptqs":0,"zwrks":0,"zwbzs":0,"sfwtj":null,"sfwtq":null,"sfybz":null,
"kyjcqk":null,"kysy":null,"handprintList":null,"sceneBioEvidences":null,"sceneFootprints":null,"ignore":null,
"sfzz":null,"techId":null,"sortOrder":null,"sortName":null,"orderByString":null,"zcCount":null,"ytjCount":null,
"bhgCount":null,"bwzCount":null,"dwCount":null,"grCount":null,"yclCount":null,"wclCount":null,"tqSqlString":null,
"evidenceExtractFlag":null,"evidenceExtrCorrectiveFlag":null,"evidenceCompFlag":null,"evidenceCompCorrectiveFlag":null,
"ifSendSMS":null,"overdueFlag":null,"zwtj":null,"zjtj":null,"dnasj":null,"zwtq":null,"zjtq":null,"dnatq":null,
"jztq":null,"tqFlag":null,"remark":null,"sfcl":null}],"pages":null,"operates":null}
```
