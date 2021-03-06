#参数默认值
`function func(a,b=3,c=function(){})`
若中间参数指定默认值，后面没指定，要显式的传入undefined来使用默认值
#rest参数
...变量名，用于获取多余的参数
* 是一个数组
* rest参数之后不能有其他参数
* length属性不包括rest参数，length统计的只是命名参数的数量

#name属性
* 每个函数都有一个name属性
* 函数表达式名字比被赋值的变量权重高
* setter、getter函数带前缀set、get
* bind()创建的带有bound前缀
* 通过Function构造函数创建的名字为anonymous

#new.target
若函数是作为构造函数调用，指向构造函数；否则为undefined

#块级函数
* 严格模式会被提升到块的顶部
* 非严格模式会被提升到全局作用域

#箭头函数
* 函数体内的this对象，就是定义时所在的对象，而不是使用时所在的对象。箭头函数内部没有this，引用的外层的this
* arguments、super、new.target也是不存在的
* 不可以当作构造函数
* 不可以使用arguments对象，该对象在函数体内不存在。如果要用，可以用 rest 参数代替。
* 不可以使用yield命令，因此箭头函数不能用作 Generator 函数。

#尾调用优化
* 尾调用是指某个函数的最后一步是调用另一个函数
* 尾调是函数的最后一步操作，不需要保留外层函数的调用帧，只要直接用内层函数的调用帧，取代外层函数的调用帧就可以了
* 只有不再用到外层函数的内部变量，内层函数的调用帧才会取代外层函数的调用帧
* 仅在严格模式下开启
#尾递归
