#rest参数
...变量名，用于获取多余的参数
* 是一个数组
* rest参数之后不能有其他参数
* length属性不包括rest参数

#箭头函数
* 函数体内的this对象，就是定义时所在的对象，而不是使用时所在的对象。箭头函数内部没有this，引用的外层的this
* arguments、super、new.target也是不存在的
* 不能用call、apply、bind等方法
* 不可以当作构造函数
* 不可以使用arguments对象，该对象在函数体内不存在。如果要用，可以用 rest 参数代替。
* 不可以使用yield命令，因此箭头函数不能用作 Generator 函数。