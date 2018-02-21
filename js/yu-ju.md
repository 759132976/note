#for语句
for里面只写两个分号可以实现无限循环
#for-in语句
用来枚举对象的属性，顺序不可预测，使用for-in之前要先检查对象的值是不是null或undefined，__Safari3以前版本的for-in有个bug会导致某些属性返回两次__
#label语句
`label:statement`
一般与循环语句配合使用，可以由break或continue引用
#with语句
将代码的作用于设置到特定的对象中
`with(expression) statement;`
#swithch语句
break跳出switch，省略会执行下一个case，default