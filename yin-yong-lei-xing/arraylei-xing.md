# 创建

new Array\(\)  
数组字面量，不会调用Array构造函数  
数组的length不是只读的，可以通过修改length移除或添加数组项

# 检测数组

instanceof  
Array.isArray\(\)

# 转换方法

* toString\(\)返回数组中每个值得字符串形式拼接的以逗号分隔的字符串，调用数组每一项的toString\(\)方法
* toLocaleString\(\)返回数组中每个值得字符串形式拼接的以逗号分隔的字符串，调用数组每一项的toLocaleString\(\)方法
* valueOf\(\)返回的还是数组
* join方法，接收一个参数，用作分隔符的字符串，返回包含所有项的字符串

# 栈方法

push、pop

# 队列方法

shift、push  
unshift、pop  
push和unshift返回修改后的长度，shift和pop返回弹出的项

# 重排序方法

reverse、sort  
sort会调用每项的toString方法然后比较字符串，默认升序，也可以接受比较函数

```
function compare(value1,value2) {
    if (value1 < value2) {
        return -1;
    } else if (value1 > value2) {
        return 1;
    } else {
        reutrn 0;
    }
}
```

第一个参数在第二个之前返回负数，之后返回正数，相等返回0

```
function compare(value1,value2) {
    return value2-value1;
}
```



