# Global对象

#### URI编码方法

encodeURI，用于整个URI，不会对特殊字符编码  
encodeURIComponent，URI某一段，对任何非标准字符编码**（常用）**  
decodeURI  
decodeURIComponent

#### eval方法

eval类似ECMAScript解析器，接收要执行的ECMAScript字符串作为参数，在eval中创建的变量和函数不会提升

#### window对象

浏览器里承担Global对象的角色

# Math对象

#### Math对象的属性

E LN10 LN2 LOG2E LOG10E PI SQRT1\_2 SQRT2

#### min\(\)和max\(\)方法

#### 舍入方法

ceil向上舍入  
floor向下舍入  
round标准舍入，四舍五入

#### random方法

返回介于0和1之间的随机数

```js
function selectFrom(lowerValue, upperValue) {
    return Math.floor(Math.random() * (upperValue-lowerValue+1) + lowerValue)
}
```



