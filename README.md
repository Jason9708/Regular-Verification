### 验证函数
```
validatieReg:function(arg){
    const Reg = /???/   // ??? 正则表达式
    if(!Reg.test(arg)){
        console.log('errorMsg')
        return false
    }
    return true
}
```


### Regular Collection
#### 数字类
```
验证数字：^[0-9]*$ 
验证n位的数字：^\d{n}$ 
验证至少n位数字：^\d{n,}$ 
验证m-n位的数字：^\d{m,n}$ 
验证零和非零开头的数字：^(0|[1-9][0-9]*)$ 
验证有两位小数的正实数：^[0-9]+(.[0-9]{2})?$ 
验证有1-3位小数的正实数：^[0-9]+(.[0-9]{1,3})?$ 
验证非零的正整数：^\+?[1-9][0-9]*$ 
验证非零的负整数：^\-[1-9][0-9]*$ 
验证非负整数（正整数 + 0） ^\d+$ 
验证非正整数（负整数 + 0） ^((-\d+)|(0+))$ 
整数：^-?\d+$ 
非负浮点数（正浮点数 + 0）：^\d+(\.\d+)?$ 
正浮点数 ^(([0-9]+\.[0-9]*[1-9][0-9]*)|([0-9]*[1-9][0-9]*\.[0-9]+)|([0-9]*[1-9][0-9]*))$ 
非正浮点数（负浮点数 + 0） ^((-\d+(\.\d+)?)|(0+(\.0+)?))$ 
负浮点数 ^(-(([0-9]+\.[0-9]*[1-9][0-9]*)|([0-9]*[1-9][0-9]*\.[0-9]+)|([0-9]*[1-9][0-9]*)))$ 
浮点数 ^(-?\d+)(\.\d+)?$
零和非零开头的数字：^(0|[1-9][0-9]*)$
正数、负数、和小数：^(-|+)?d+(.d+)?$
有两位小数的正实数：^[0-9]+(.[0-9]{2})?$
```
#### 信息类
```
11位有效手机号：^[1][3,4,5,6,7,8,9][0-9]{9}$
固定电话（区号8xxxxxxx）：^(\(\d{3,4}\)|\d{3,4}-|\s)?\d{7,14}$
手机号码 + 固定电话：^((0\d{2,3}-\d{7,8})|(1[3456789]\d{9}))$
Email：^[A-Za-z0-9\u4e00-\u9fa5]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$
InternetURL：^http://([\w-]+\.)+[\w-]+(/[\w-./?%&=]*)?$ ；^[a-zA-z]+://(w+(-w+)*)(.(w+(-w+)*))*(?S*)?$ 
邮编：^[1-9][0-9]{5}$
身份证：(^\d{15}$)|(^\d{18}$)|(^\d{17}(\d|X|x)$)
银行卡（15+16+19）：^([1-9]{1})(\d{14}|\d{18}|\d{15})$
```
#### 字符类
```
验证长度为n的字符：^.{n}$ 
验证由26个英文字母组成的字符串：^[A-Za-z]+$ 
验证由26个大写英文字母组成的字符串：^[A-Z]+$ 
验证由26个小写英文字母组成的字符串：^[a-z]+$ 
验证由数字和26个英文字母组成的字符串：^[A-Za-z0-9]+$ 
验证由数字、26个英文字母或者下划线组成的字符串：^\w+$ 
验证用户密码:^[a-zA-Z]\w{5,17}$ 正确格式为：以字母开头，长度在6-18之间，只能包含字符、数字和下划线。 
验证是否含有 ^%&',;=?$\" 等字符：[^%&',;=?$\x22]+ 
验证汉字：^[\u4e00-\u9fa5],{0,}$ 
中文、英文、数字但不包括下划线等符号：^[u4E00-u9FA5A-Za-z0-9]+$ 或 ^[u4E00-u9FA5A-Za-z0-9]{2,20}$
中文、英文、数字包括下划线：^[u4E00-u9FA5A-Za-z0-9_]+$
禁止输入含有~的字符：[^~x22]+
首尾空白字符的正则表达式：^s*|s*$或(^s*)|(s*$)  → 可以用来删除行首行尾空白字符
```
#### 日期
```
验证XXXX-XX-XX格式日期：^(\d{4})(-)(\d{2})(-)(\d{2})$
```