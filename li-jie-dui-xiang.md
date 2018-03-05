#属性类型
分为数据属性和访问器属性两类
####数据属性
[[Configurable]]
[[Enumerable]]
[[Writeable]]
[[Value]]

用Object.defineProperty来修改，接收属性所在的对象、属性的名字和描述符对象为参数，一旦configurable改为false就改不回去了，调用该方法时默认值都是false

####访问器属性
[[Configurable]]
[[Enumerable]]
[[Get]]
[[Set]]

不能直接定义，必须使用Object.defineProperty定义

#定义多个属性
Object.defineProperties，两个对象作为参数：第一个对象为要添加和修改属性的对象、第二个对象的属性与第一个对象中要添加或修改的属性一一对应。

#读取属性的特性
Object.getOwnPropertyDescriptor，接收属性所在的对象和属性描述符作为参数，返回一个对象，只能用于实例属性，要获得原型属性描述符要在原型对象上调用。