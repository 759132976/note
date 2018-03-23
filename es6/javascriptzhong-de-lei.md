# 类的声明

```js
class Person {
    constructor(name) {
        this.name = name;
    }
    sayName() {
        console.log(this.name);
    }
}
```
* 类声明不能被提升
* 类声明中的代码自动运行在严格模式下
* 类中所有方法不可枚举
* 不通过new调用会导致错误
* 在类中修改类型会出错，在外部可以修改

#静态方法
static关键字
#继承和派生类
* extends关键字，在构造函数中调用super()
* 必须在使用this之前调用super()