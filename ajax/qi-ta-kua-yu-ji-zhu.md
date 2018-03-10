# 图像Ping

动态创建图像，使用onload和onerror事件处理程序来确定是否响应

```js
var img = new Image();
img.onload = img.onerror = function () {
    alert('Done!');
};
img.src = 'http://www.example/com/test?name=Nicholas';
```

图像Ping最常用于跟踪用户点击页面或动态广告的曝光次数。有两个缺点：一是只能发送get请求，二是无法访问服务器的响应文本。图像Ping只能用于浏览器与服务器间的单向通信

# JSONP

* JSONP（JSON with padding，填充式JSON或参数式JSON）
* 和JSON差不多，是被包含在函数调用中的JSON

```js
callback({"name":"Nicholas"});
```

* 由两部分组成：回调函数和数。回调函数是响应到来时应该在页面调用的函数，一般是在请求中指定的;数据就是传入回调函数中的JSON

  [http://freegeoip.net/json/?callback=handleResponse](http://freegeoip.net/json/?callback=handleResponse)

* 通过动态创建script元素来使用，为src指定一个跨域url

```js
function handleResponse(response){
    alert ("You're at IP address " + response.ip + ", which is in " + response.city + ", "+ response.region_name);
}
var script = document.createElement("script");
script.src = "http://freegeoip.net/json/?callback=handLeResponse"; 
document.body.insertBefore(script, document.body.firstChild);
```

* 缺点：
    * 如果其他域不安全，很可能会在响应中夹带恶意代码
    * 不容易确定JSONP请求失败

#Comet
也称为服务器推送，是一种服务器向页面推送数据的技术，近乎实时
####实现方式
* 长轮询：页面发起请求，服务器一直保持连接打开，直到有数据可发送。发送完数据之后，浏览器关闭连接随机又发起新请求。
* 流：浏览器向服务器发送一个请求，服务器保持连接打开，周期性的向浏览器发送数据。通过监听readstatechange事件和检测readState是否为3可以利用XHR实现HTTP流