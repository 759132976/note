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

# 问答题

#### promise

#### 常见的浏览器兼容问题

#### 三次握手和四次挥手

![](/assets/三次握手.jpg)  
如果两次握手客户端发送请求时失效，客户端会重新发送请求，服务器接收到请求后双方建立连接，结束后断开连接。若这时失效的请求到达，服务器就会一直等待，浪费资源。  
![](/assets/四次挥手.jpg)

#### js跨域

[http://www.cnblogs.com/rainman/archive/2011/02/20/1959325.html\#m3](http://www.cnblogs.com/rainman/archive/2011/02/20/1959325.html#m3)

#### 盒模型

#### MVC和MVVM

[http://www.ruanyifeng.com/blog/2015/02/mvcmvp\_mvvm.html](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)

# 程序题

#### 找出1到100间的所有完全数（除了本身以外的因数和等于其本身）

```js
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

#### 输出10行的杨辉三角形

```js
var result = [];
for (let i = 1; i < 11; i++) {
  result[i] = [];
  result[i][1] = 1;
  result[i][i] = 1;
}
for (let i = 3; i < 11; i++) {
  for (let j = 2; j < i; j++) {
    result[i][j] = result[i - 1][j - 1] + result[i - 1][j]
  }
}
for (let i = 1; i < 11; i++) {
  console.log(result[i].join(' '));
}
```

* js二维数组的用法，不能result\[i,j\]要result\[i\]\[j\],用的时候注意初始化：result\[i\]=\[\]
* console.log\(\)自动换行



