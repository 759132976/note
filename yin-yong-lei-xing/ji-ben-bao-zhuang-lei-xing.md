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
*    
    *    slice，substr，substring，返回一个子字符串。接收一或两个参数，第一个指定子字符串开始位置，第二个参数表示子字符串到哪里结束。
    *    slice和substring第二个参数指定子字符串最后一个字符后面的位置，substr指定返回的字符的个数
    *    传入正数时差别不大，传入负数的话，slice会把参数与字符串长度相加；substr会将负的第一个参数加上字符串长度，负的第二个参数转换为0；substring会把所有负数转换为0
*    indexOf、lastIndexOf，送字符串中搜索给定的子字符串，返回子串位置。可选的第二个参数表示搜索的起始位置
*    trim，创建一个字符串副本，删除前置和后缀的所有空格
*    toLowerCase、toLocaleLowerCase、toUpperCase、toLocaleUpperCase
*    模式匹配
    *    match，本质与exec相同，接收一个参数，正则表达式或者RegExp对象
    *    search，参数和match相同，返回第一个匹配项的索引，从开头向后查找
    *    replace，替换字符串，第一个参数是RegExp对象或者字符串，第二个参数是一个字符串或一个函数。如果第一个参数是字符串只会替换第一个子字符串，替换所有要用正则
    *    split，基于指定的分隔符将字符串分割成多个子串，结果放到数组中，分隔符可以是字符串也可以是RegExp对象。可选的第二个参数指定数组的大小
*    localCompare，比较两个字符串，并返回
    *    字符串在字母表中排在参数之前，返回负数
    *    字符串等于参数字符串，0
    *    字符串在字母表中排在参数之后，返回正数
*    fromCharCode，接收一个或多个字符编码，转换成字符串