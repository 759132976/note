ECMAScript只支持实现继承，主要依靠原型链实现
#原型链
将一个构造函数的原型指向另一个类型的实例
####别忘记默认的原型
所有引用类型默认继承了Object，默认原型会有一个指针指向Object.prototype，所有自定义类型都会继承toString、valueOf等默认方法
####确定原型和实例的关系
instanceof
isPrototypeOf
####谨慎的定义方法
* 子类型要重写或者添加某个方法，一定要放在替换原型的语句之后，不然会被覆盖
* 不能通过对象字面量创建原型方法，否则会重写原型链

####原型链的问题
* 引用类型的原型属性会被所有实例共享，某个实例改变了原型中的方法会导致其他实例中的方法发生改变。
* 创建子类型实例的时候不能向超类型的构造函数中传递参数

#借用构造函数（伪造对象或经典类型）
在子类型构造函数的内部调用超类型构造函数，通过apply或call调用
####传递参数
可以在子类型构造函数向超类型的构造函数传递参数，通过apply和call的第二个参数
####借用构造函数的问题
方法在构造函数中定义了，无法进行复用，而且在超类型的原型中定义的方法对子类型是不可见的
#组合继承（伪经典继承）
将原型链和借用构造函数组合，使用原型链实现对原型属性和方法的继承，通过借用构造函数实现对实例属性的继承。
#原型式继承
Object.create,创建一个临时的构造函数，将传入的对象作为该构造函数的原型，返回临时构造函数的实例，会创建一个被寄生函数的副本。
#寄生式继承
创建一个仅用于封装继承过程的函数，在内部以某种方式增强对象，通过该方法添加的函数也不能复用。
#寄生组合式继承
* 组合继承会调用两次超类型的构造函数
* 用寄生式继承来继承超类型的原型，再将结果指定给子类型的原型