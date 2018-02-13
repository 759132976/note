####基本数据类型
string、null、undefined、number、boolean
####复杂数据类型
object

null == undefined //ture

#Number
####最大值和最小值
Number.MAX_VALUE
Number.MIN_VALUE
####无穷
Infinity，可以用isFinite()判断
####NaN
NaN == NaN //false
isNaN()会尝试将值转换为数值，无法转换返回false
####类型转换
parseInt()最好指定第二个参数：转换时使用的基数（多少进制）
parseFloat()只解析十进制

#String
字符串是不可变的
####类型转换
toString()，可以指定基数，null和undefined没有
String()，任何类型

#Object
####创建
new Object()
####方法和属性
Constructor
hasOwnProperty(propertyName)
isPrototypeOf(object)
propertyIsEnumerable(propertyName)
toLocaleString()
toString()
valueOf()

