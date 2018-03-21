* let声明的变量只在块级作用域内有效
* let不存在变量提升
* 存在暂时性死区。在代码块内，使用let命令声明变量之前，该变量都是不可用的，不受外部影响。typeof有可能会导致错误

```js
typeof x; // ReferenceError
let x;
```

```js
function bar(x = y, y = 2) {
  return [x, y];
}

bar(); // 报错
```

```js
// 不报错
var x = x;

// 报错
let x = x;
// ReferenceError: x is not defined
```

* 不允许重复声明
* let实质上添加了块级作用域
* 避免在块级作用域中声明函数，如有需要使用函数表达式
* 不会添加为全局对象的属性



