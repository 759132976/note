# 1.垂直水平居中absolute为什么四个方向都是0?

绝对定位的元素对立的方向都有值时会触发流体特性，自适应于包含块的padding-box宽度

# 2.jquery插件怎么写？

* $.extend\(\)扩展
* $.fn.xxx,为jquery添加新的方法

# 3.$.fn是什么？

jquery.prototype

# 4.怎样复制一个数组

```js
b = a.slice(0);
b = a.contact();
b = [...a];
```

#5.原型链，object.prototype.\_\__proto_\_\_ = null
* Function.\_\_proto\_\_ == Function.prototype,Function的构造函数是Function本身
* Function.prototype.\_\_proto\_\_ == Object.prototype,Function.prototype是一个对象也是一个函数，构造函数的prototype的proto指向Object.prototype
* Object.\_\_proto\_\_ == Function.prototype，Object是一个函数

#6.模块化开发——浏览器（同步加载和异步加载）
