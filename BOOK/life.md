## Phone
****
#### 11位有效手机号
```
validatieMobPhone:function(mobphoneNumber){
    const mobphoneReg = /^[1][3,4,5,6,7,8,9][0-9]{9}$/
    if(!mobphoneReg.test(mobphoneNumber)){
        console.log('请输入11位有效合法手机号')
        return false
    }
    return true
}
```

#### 固定电话（区号-8xxxxxxx）
```
validatieTelPhone:function(telphoneNumber){
    const telphoneReg = /^(\(\d{3,4}\)|\d{3,4}-|\s)?\d{7,14}$/
    if(!telphoneReg.test(telphoneNumber)){
        console.log('请输入有效固定手机号码')
        return false
    }
    return true
}
```

#### 手机号码 + 固定电话
```
validatiePhone:function(phoneNumber){
    const phoneReg = /^((0\d{2,3}-\d{7,8})|(1[3456789]\d{9}))$/
    if(!phoneReg.test(phoneNumber)){
        console.log('请输入有效联系号码')
        return false
    }
    return true
}
```


## Email
****
```
validatieEmail:function(email){
    const emailReg = /^[A-Za-z0-9\u4e00-\u9fa5]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$/
    if(!emailReg.test(email)){
        console.log('请输入有效电子邮箱')
        return false
    }
    return true
}
```

## 邮编
****
```
validatieZipCode:function(zipCode){
    const zipCodeReg = /^[1-9][0-9]{5}$/
    if(!zipCodeReg.test(zipCode)){
        console.log('请输入有效邮编地址')
        return false
    }
    return true
}
```

## 身份证
****
```
validatieIdCard:function(idCard){
    const idCardReg = /(^\d{15}$)|(^\d{18}$)|(^\d{17}(\d|X|x)$)/
    if(!idCardReg.test(idCard)){
        console.log('请输入有效邮编地址')
        return false
    }
    return true
}
```

## 银行卡 （15位或者16位或者19位）
****
```
validatieBankCard:function(bankCard){
    const bankCardReg = /^([1-9]{1})(\d{14}|\d{18}|\d{15})$/
    if(!bankCardReg.test(bankCard)){
        console.log('请输入有效邮编地址')
        return false
    }
    return true
}
```