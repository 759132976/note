特殊的引用类型：Boolean，String，Number。基本包装类型的对象只存在于代码执行的瞬间，然后立即被销毁，不建议显式创建基本包装类型的对象
#Boolean类型
*    重写了valueOf方法，返回ture或false；重写了toString方法，返回"true"和"false"
*    在布尔表达式中使用布尔类型的对象会被转换为true
*    typeof，基本类型返回boolean，引用类型返回object
*    instanceof Boolean测试引用类型返回true，测试基本类型返回false
#Number类型
*    重写了valueOf，返回对象表示的基本类型的值；重写了toString和toLocaleString，返回字符串形式的值
*    toString传递参数表示基数
*    toFixed，按指定的小数位返回字符串表示
*    toExponential，返回指数表示的字符串形式，接收一个参数小数位数
*    toPrecision，可能返回固定大小（fixed）形式，也可能返回指数形式，接收一个参数即表示数值的所有数字的位数（不包含指数部分）
#String类型
*    length，字符串中包含多少字符
*    charAt和charCodeAt，接收一个参数，基于0的字符位置。charAt返回单字符串形式，charCodeAt返回字符编码
*    contact，拼接字符串