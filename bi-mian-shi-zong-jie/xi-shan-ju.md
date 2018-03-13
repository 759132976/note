# 2019.3.13

#### 填空

* null+1 // 1  
* undefined+1    // NaN  
* typeof NaN     // 'Number'  
* * typeof 4\*\_'a'     // 'NaN'
  * typeof \(4\*'a'\)  // 'Number'
  * typeof优先级高于+-\*/低于括号  所以顺序是typeof 4返回'number'再乘'a'返回'NaN'

![](/assets/西山居1.jpg)
![](/assets/西山居2.jpg)

* new后面只跟函数，new是从右向左的

```js
function fn(a) {
  console.log(typeof a)
  var a = 2;

  function a() {}
  console.log(typeof a)
}
fn(1)
```