事件和回调可以实现异步编程

# 基础知识

Promise相当于异步操作结果的占位符，让函数返回一个Promise对象  
`let promist = readFile("example.txt")`

#### 生命周期

* pending：进行中
* fulfilled：成功
* rejected：失败

  #### then\(\)方法

  每个Promise都有then\(\)方法，两个参数：第一个是状态变为fulfilled时调用的函数，第二个是状态变为rejected时调用的函数

  #### catch\(\)方法

  一个参数，拒绝时调用的函数

  # 创建未完成的Promise

* Promise构造函数，接受一个参数：包含初始化Promise代码的执行器函数。执行器接受两个参数，分别是resolve\(\)函数和reject\(\)函数。
* 执行器会立即执行，调用resolve\(\)或者是reject会\(\)向任务队列添加一个任务延后执行，then\(\)和catch\(\)是异步的

```js
let promise = new Promise(function(resolve,reject) {
    console.log("Promise");
    resolve();
}
promise.then(function(){
    console.log("Resolved");
})
console.log("Hi!");

Promise
Hi
Resolved
```



