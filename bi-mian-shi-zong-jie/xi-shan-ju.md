# 2019.3.13

#### 填空

* null+1 // 1  
* undefined+1    // NaN  
* typeof NaN     // 'Number'  
* * typeof 4\*\_'a'     // 'NaN'
  * typeof \(4\*'a'\)  // 'Number'
  * typeof优先级高于+-\*/低于括号  所以顺序是typeof 4返回'number'再乘'a'返回'NaN'

```js
function F() {
  foo = function () {
    alert(1)
  }
  return this
}
F.foo = function () {
  alert(2)
}
F.prototype.foo = function () {
   alert(3)
}
var foo = function () {
  alert(4)
}

function foo() {
  alter(5)
}
```
* * F.foo() // 2
  * foo() // 4
  * F().foo() // 1
  * foo() // 1
  * new F.foo() // 2
  * new F().foo() // 3
  * new new F().foo() // 3

