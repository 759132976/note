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

5.原型链，object.prototype.\_\__proto_\_\_ = null
Function.\_\_proto\_\_ == Function.prototype
Object.\_\_proto\_\_ == Function.prototype