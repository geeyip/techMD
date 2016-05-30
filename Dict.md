## 基本用法

**HTML 代码**

``` html
<dict dict-type="tree" dict-root="GXSDM" name="fadd" id="fadd"/>
```

**JAVASCRIPT 代码**

``` javascript
//字典初始化
$("#fadd").dict();

//字典初始化并且赋值
$("#fadd").dict().dictSelect("330100");

//字典赋值
$("#fadd").dictSelect("330100");

//字典取值
$("#fadd").val();
```

**参数说明**

`dict-type` 字典展示类型，必填。可选的值有 `tree`、`select`、`checkbox`, 分别代表树形、下拉、多选框字典

`dict-root`字典代码类型，必填。大小写都可以

## 返回中文

``` html
<dict dict-type="tree" dict-root="GXSDM" name="fadd" id="fadd" return-value="tree"/>
```

`return-value = "true"` 时， 字典返回中文，树形、下拉、多选框都适用

### 树形字典多选

``` html
<dict dict-type="tree" dict-root="GXSDM" name="fadd" id="fadd" dict-multiple="tree"/>
```

`dict-multiple="tree"`时，树形字典支持多选。

### 下拉字典非空

``` html
<dict dict-type="tree" dict-root="GXSDM" name="fadd" id="fadd" empty="false"/>
```

`empty="false"`时，下拉字典没有空选项。

### 自定义数据

``` javascript
var data = [
  {key: '1', value: '是', parentKey: ''}， 
  {key: '0', value: '否', parentKey: ''}
]; 
$("#fadd").dict(data);
```

### 其他说明

无