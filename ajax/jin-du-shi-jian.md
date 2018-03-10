* loadstart：接收到响应数据第一个字节时触发
* progress：接收响应期间持续触发，据此创建进度指示器
* error：请求发生错误时触发
* abore：调用abort终止连接时触发
* load：接收到完整的数据时触发，代替readystatechange事件
* loadend：通信完成或触发error、abort、load后触发

每个请求都从loadstart开始，然后一个或多个progress事件，然后error、abort或load，最后loadend