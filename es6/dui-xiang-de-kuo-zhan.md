#Object.is
比较两个值严格相等，与===基本一致，但是+0不等于-0，NaN等于NaN
#Object.assign
* 合并对象，将源对象的所有可枚举属性，复制到目标对象，第一个参数是目标对象，后面的参数是源对象
* 只能拷贝源对象的自身属性（不拷贝继承属性），也不拷贝不可枚举的属性
* 属性名为 Symbol 值的属性，也会被Object.assign拷贝

#属性的遍历
ES6 一共有 5 种方法可以遍历对象的属性。
* for...in循环，遍历对象自身的和继承的可枚举属性（不含 Symbol 属性）。
* Object.keys(obj)，返回一个数组，包括对象自身的（不含继承的）所有可枚举属性（不含 Symbol 属性）的键名。
* Object.getOwnPropertyNames(obj)，返回一个数组，包含对象自身的所有属性（不含 Symbol 属性，但是包括不可枚举属性）的键名。
* Object.getOwnPropertySymbols(obj)，返回一个数组，包含对象自身的所有 Symbol 属性的键名。
* Reflect.ownKeys(obj)，返回一个数组，包含对象自身的所有键名，不管键名是 Symbol 或字符串，也不管是否可枚举。