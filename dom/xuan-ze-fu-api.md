#选择符API
* querySelector()，返回第一个，没有返回null
* querySelectorAll(),返回NodeList对象
* matchesSelector()，参数css选择符，元素与选择符匹配返回true

#HTML5
####与类相关的扩充
* getElementsByClassName()
* 元素的classList属性
    * add
    * contains
    * remove
    * toggle

####焦点管理
* document.activeElement，始终引用获取了焦点的元素
* document.hasFocus()，文档是否获取了焦点

####自定义数据属性
* 为元素提供与渲染无关的信息或者提供语义信息，以data-开头
* 通过元素的dataset访问

####插入标记
* innerHTML
* outerHTML
* insertAdjacentHTML(),两个参数，插入位置和要插入的html文本，位置是beforebegin、afterbegin、beforeend、afterend中的一个

####scrollIntoView()方法
调用元素出现在视口中，true或不传，元素顶部与视口顶部尽可能平齐，false元素会尽可能全部出现在视口（可能的话底部与视口平齐）