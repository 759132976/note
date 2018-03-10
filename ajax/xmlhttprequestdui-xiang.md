IE7+：new XMLHTTPRequest()
#XHR用法
* open，三个参数，要发送的请求的类型、请求的URL和表示是否异步发送*的布尔值，该方法不会真正发送请求，只是启动一个请求以备发送
* send，用来发送特定的请求，接收一个参数，作为请求主体发送的数据，如果不需要传入null。
* 收到响应后响应的数据会自动填充XHR对象的属性：
    * responseText：作为响应主体被返回的文本
    * responseXML：响应类型是"text/xml"或"application/xml"，保存响应的XML DOM文档
    * status： 响应的HTTP状态
    * statusText： HTTP状态的说明
* 异步发送，检查readyState属性：
    * 0：未初始化，未调用open方法
    * 1：启动，调用open未调用send
    * 2：发送，已调用send，未收到响应
    * 3：接收，接受到部分响应数据
    * 4：完成，接收到全部响应数据
    
 每次readState属性改变会触发readstatechange事件，在调用open之前指定onreadystatechange事件处理程序
* 接收到响应之前可以调用abort方法取消异步请求
#HTTP头部信息
* 默认情况发送XHR请求时会发送：
    * Accept：浏览器能够处理的内容类型
    * Accept-Charset：浏览器能够显示的字符集
    * Accept-Encoding：浏览器能够处理的压缩编码
    * Accept-Language：浏览器当前设置的语言
    * Connection：浏览器与服务器之间连接的类型
    * Cookie：当前页面设置的任何Cookie
    * Host：发出请求的页面所在的域
    * Referer：发出请求的页面的URI
    * User-Agent：浏览器的用户代理字符串
* 使用setRequestHeader方法设置自定义头信息，接收两个参数：头部字段名称和头部字段值，在调用open之后send之前调用
* 调用getResponseHeader方法并传入头部字段名称可以取得响应的响应头信息，调用getAllResponseHeaders可以获得包含所有头部信息的长字符串。

#get请求
常用于向服务器查询某些信息，可以直接将查询字符串参数追加到url末尾。对于XHR，查询字符串必须经过正确的编码，使用encodeURIComponent编码。
#post请求
* 通常用于向服务器发送应该被保存的数据，应该把数据作为请求的主体提交
* 模仿表单提交：将Content-Type请求头设置为application/x-www-form-urlencoded，对表单数据进行序列化。

post请求消耗的资源比get多一些，get请求的速度最快可以达到post请求的两倍
