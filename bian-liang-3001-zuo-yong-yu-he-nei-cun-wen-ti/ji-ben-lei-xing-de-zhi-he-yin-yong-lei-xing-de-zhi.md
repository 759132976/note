基本类型值：5种基本数据类型，按值访问，可以操作实际值，栈
引用类型值：对象，操作对象的引用，堆
#动态的属性
引用类型的值可以添加或删除或修改属性和方法，基本类型的值不可以
#复制变量值
基本类型值复制实际值，操作独立；引用类型值复制的是指针，两个指向同一个对象，改变会相互影响
#传递参数
函数参数是按值传递的，如果是基本类型值，会将实际值复制，所以参数和外部变量相互独立；如果是引用类型的值，会传递地址引用，参数的变化会反映在外部
```
function setName(obj) {
    obj.name = 'gcd';
    obj = new Object();
    obj.name = 'cc';
}
var person = new Object();
setName(person);
alert(person.name); // gcd
```
以上代码证明参数是按值传递，重写obj时指向了另一个对象
#检测类型
typeof：字符串、数值、布尔值、undefined，对象或者null都返回"object"
instanceof：variable instanceof constructor