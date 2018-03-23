# 类的声明

```js
class Person{
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