## n位数字
****
```
validatieNumberSum:function(number){
    const numberSumReg = /^\d{n}$/    // n为几位
    if(!numberSumReg.test(number)){
        console.log('请输入n位数字')
        return false
    }
    return true
}
```

## 至少n位数字
****
```
validatieLessNumberSum:function(number){
    const lessNumberSumReg = /^\d{n,}$/    // n为几位
    if(!lessNumberSumReg.test(number)){
        console.log('请至少输入n位数字')
        return false
    }
    return true
}
```

## m-n位数字
****
```
validatieRangeNumberSum:function(number){
    const rangeNumberSumReg = /^\d{m,n}$/    // m，n为几位
    if(!rangeNumberSumReg.test(number)){
        console.log('请至少输入m-n位数字')
        return false
    }
    return true
}
```

## 正整数 + 0
****
```
validatieIsNumber:function(number){
    const isNumberReg = /^(0|[1-9][0-9]*)$/
    if(!isNumberReg.test(number)){
        console.log('请输入正整数')
        return false
    }
    return true
}
```

## 非零正整数
****
```
validatiePosNoZero:function(number){
    const posNoZeroReg = /^\+?[1-9][0-9]*$/
    if(!posNoZeroReg.test(number)){
        console.log('请输入非零正整数')
        return false
    }
    return true
}
```

## 非负整数 （正整数 + 0）
****
```
validatieNonnegativeInteger:function(number){
    const nonnegativeIntegerReg = /^(0|[1-9][0-9]*)$/
    if(!nonnegativeIntegerReg.test(number)){
        console.log('请输入非负整数')
        return false
    }
    return true
}
```
## 非正整数 （负整数 + 0）
****
```
validatieNonpositiveInteger:function(number){
    const nonpositiveIntegerReg = /^((-\d+)|(0+))$/
    if(!nonpositiveIntegerReg.test(number)){
        console.log('请输入非正整数')
        return false
    }
    return true
}
```

## 负整数 （不包括0）
****
```
validatieNegativeInteger:function(number){
    const negativeIntegerReg = /^(-[1-9][0-9]*)$/
    if(!negativeIntegerReg.test(number)){
        console.log('请输入负整数')
        return false
    }
    return true
}
```

## 整数
****
```
validatieInteger:function(number){
    const integerReg = /^-?\d+$/
    if(!integerReg.test(number)){
        console.log('请输入整数')
        return false
    }
    return true
}
```

## 非负浮点数 (正浮点数 + 0)
****
```
validatieNonnegativeFloat:function(number){
    const nonnegativeFloatReg = /^\d+(\.\d+)?$/
    if(!nonnegativeFloatReg.test(number)){
        console.log('请输入非负浮点数')
        return false
    }
    return true
}
```
