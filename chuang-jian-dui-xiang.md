# 工厂模式

无法识别对象

# 构造函数模式

与工厂模式不同：

* 没有显示创建对象
* 直接将属性和方法赋给this
* 没有return

new过程：

* 创建一个新对象
* 将构造函数的作用于赋给新对象
* 执行构造函数中的代码
* 返回新对象

可以使用constructor属性和instance of来检测对象类型

#### 将构造函数作为函数

构造函数  
普通函数 window  
在另一个对象作用域使用  call、apply等

#### 构造函数的问题

每个方法都要重新创建一遍

# 原型模式

每个函数都有一个property属性，指向一个对象，对象包含由特定类型的所有实例共享的属性和方法

#### 理解原型对象

* 创建函数时会创建property属性指向原型对象，原型对象会有一个constructor属性指向property属性所在的函数，Person.property.constructor指向Person
* 每个函数的实例内部有个指针指向原型对象，在Firefox、Safari、和Chrome中可以通过\_\__proto\_\__来访问



