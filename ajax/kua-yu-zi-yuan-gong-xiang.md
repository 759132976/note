* 默认XHR对象只能访问和包含它的页面位于同一个域中的资源。
* CORS（Cross-Origin Resource Sharing）思想，使用自定义的请求头让浏览器和服务器沟通来决定请求成功还是失败。
* 添加额外的Origin头部，包含请求页面的源信息，服务器根据这个头信息来决定是否响应，若可接受，在Access-Control-Allow_Origin头部中回发相同的源信息。

#IE对CORS的实现
引入了XDR（XDomainRequest类型），与XHR相似，但也有不同：
* Cookie不会随请求发送，也不会随响应返回
* 只能设置请求头的Content-Type字段
* 不能访问响应头
* 只支持get和post

####使用
* 与XHR相似，创建实例，调用open，调用send，XDR的open接收两个参数：请求的类型和URL。
* XDR请求只能异步执行
* 返回后触发load事件，响应数据保存在responseText属性中
* 接收到响应后只能访问响应的原始文本，无法确定状态码，有响应就会触发load事件，失败会触发error事件
* 可以调用abort终止
* 对于post，提供了contentType属性来表示发送数据的格式，该属性是XDR影响头信息的唯一方式

#其他浏览器对CORS的实现
通过XHR实现了对CORS的原生支持，传入绝对URL即可。
跨域XHR的限制：
* 不能使用setRequestHeader方法
* 不能发送和接收cookie
* 调用getAllResponseHeaders返回空字符串
