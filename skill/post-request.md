# 页面间 post 传参

使用 form 表单

```javascript
var form = document.createElement('form');
form.name = 'form';
form.target = '_self'; // 在当前页面跳转，默认值
form.method = 'post';
form.action = issuerUrl; // 需要跳转改页面 URL
document.body.appendChild(form);

for (var i = 0, len = data.PostDataList.length; i < len; i++) {
    var currentParamModel = data.PostDataList[i];
    var input = document.createElement('input');
    input.type = 'hidden';
    input.name = currentParamModel.ParameterName;
    input.value = currentParamModel.ParameterValue;
    form.appendChild(input);
}
form.submit();
```
