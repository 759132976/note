用来响应某个事件的函数
#HTML事件处理程序
直接写在html元素里
#DOM0级事件处理程序
为一个元素的引用指定事件处理程序，被认为是元素的方法
#DOM2级事件处理程序
* addEventListener，removeEventListener。接收三个参数：要处理的事件名、作为事件处理程序的函数和一个布尔值。布尔值为true表示在捕获阶段调用，false在冒泡阶段
* 添加多个事件处理程序会按照添加的顺序触发
* addEventListener和相应的removeEventListener参数必须一致，匿名处理程序无法移除。
* 建议添加到冒泡阶段保证兼容性

#IE事件处理程序
attachEvent和detachEvent，两个参数：事件名和事件处理程序，添加到冒泡阶段