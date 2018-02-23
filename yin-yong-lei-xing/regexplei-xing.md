#创建
*    var expression = /pattern/flags;
       pattern表示正则表达式，flags包括：
       *    g，全局模式，应用于所有字符串，不在发现第一个匹配项时停止
       *    i，不区分大小写模式
       *    m，多行模式，会继续查找下一行
       
    元字符需要被转移，包括( { [ \ ^ $ | ) ? * + . ] }，用\转义
    
*     new RegExp(),接收两个参数，要匹配的字符串模式和可选的字符串标志，两个参数都是字符串，要进行双重转义

#RegExp实例属性
*       global，布尔值，是否设置了g标志
*       ignoreCase，布尔值，是否设置了i标志
*       multiline，布尔值，是否设置了m标志
*       lastIndex，整数，开始搜索的下一个匹配项的字符位置，从0开始
*       soure，正则表达式的字符串表示，按字面量形式返回

#RegExp实例方法
* exec，专为捕获组设计，接收要应用模式的字符串，返回包含第一个匹配项信息的数组，没有匹配返回null。
       *       数组包含两个额外的属性：index和input，index表示匹配项在数组中的位置，input表示应用正则表达式的字符串。数组第一项是与整个模式匹配的字符串，其他项是与捕获组匹配的字符串。
       *       没有设置全局标志始终返回第一个匹配项的信息，lastIndex始终不变；设置了全局模式的每次都会在字符串中继续查找匹配项，lastIndex会增加
*       test，接收一个字符串参数，模式与参数匹配返回true
*       toString，toLocaleString，返回正则表达式字面量

#RegExp构造函数属性
适应于作用域中的所有正则表达式，基于所执行的最近一次正则表达式操作变化
*       input，最近一次要匹配的字符串
*       lastMatch，最近一次的匹配项
*       lastParen，最近一次匹配的捕获组
*       leftContext，input字符串中lastMatch之前的文本
*       RightContext，input字符串中lastMatch之后的文本、
*       multiline，布尔值，表示是否所有表达式都是用多行模式
*       $1...$9,储存第一..第九个捕获组
