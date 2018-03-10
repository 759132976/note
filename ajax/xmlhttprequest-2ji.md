#FormData
为序列化表单以及创建与表单格式相同的数据提供了便利。
* new FormData()，再调用append方法，接收两个参数：键和值，对应表单中字段的名字和字段值。添加键值对
* 也可以向构造函数传递表单元素填充

不必设置请求头
#超时设定
timeout属性，在规定时间内没有收到响应会触发timeout事件，调用ontimeout事件处理程序
#overrideMimeType方法
重写XHR响应的MIME类型，必须在调用send之前