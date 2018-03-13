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

* 函数提升优先级高于变量提升，不会被变量声明覆盖，但是会被变量赋值覆盖

#程序题
####找出1到100间的所有完全数
```
function find(n) {
  var sum = 1;
  var middle = Math.sqrt(n);
  for (let i = 2; i < middle; i++) {
    if (n % i == 0) {
      sum += i + n / i;
    }
  }
  if (Math.floor(middle) == middle) {
    sum += middle
  }
  if (sum == n) {
    return true
  } else {
    return false
  }
}
var result = [];
for (let i = 1; i < 101; i++) {
  if (find(i)) {
    result.push(i)
  }
}
console.log(result);
```