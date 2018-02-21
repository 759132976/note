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