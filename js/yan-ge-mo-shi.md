`"use strict";`

```
function todo() {
    "use strict";
})
```

*    严格模式下不能定义名为eval和arguments的变量，会报错。
*    严格模式下八进制的字面量是无效的
*    不允许使用with语句
*    函数名和参数名不能为eval和arguments，两个参数不能重名
*    重写arguments会导致语法错误，重写不会和命名参数同步
*    arguments.callee会出错，arguments.caller也会出错
*    不能为函数的caller属性赋值
*    未指定环境对象而调用函数，this不会转型为window，是undefined
*    外部访问不到eval中创建的变量或函数，为eval赋值会报错