#创建
let variable = Symbol()，接收参数为对symbol的描述，不能在代码中直接访问，toString()可以读取
* 是一个原始值，不能用new
* 私有名称

#Symbol共享体系
* Symbol.for()，创建一个可共享的Symbol，参数为字符串标志符：首先在全局Symbol注册表中搜索，若有直接返回已有的，否则创建一个新的并注册
* Symbol.keyFor()，可以在Symbol全局注册表中检索与Symbol有关的键