触发某个事件时会产生一个事件对象event，里面包含了所有与事件有关的信息。
#DOM中的事件对象
DOM浏览器都会将event对象传入事件处理程序。只存在于事件处理程序执行期间。
####事件的属性和方法
* this、currentTarget 表示事件处理程序当前正在处理事件的元素
* target表示事件的实际目标
* preventDefault()用来取消事件的默认行为
* stopPropagation()用来阻止事件冒泡

#IE中的事件对象
DOM0级：window.event
DOM2级：window.event，event也会作为参数传递。
HTML元素中：event的变量
