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

```js
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

```js
function compare(value1,value2) {
    return value2-value1;
}
```

简单的降序排序方法

# 操作方法

contact，接收参数并返回一个数组  
slice，接收一或两个参数，返回项的起始和结束位置，参数为负数的话由数组长度加上该参数来决定位置  
splice：

* 删除：指定第一项的位置和要删除的项数，splice\(0,2\)
* 插入：指定起始位置，0和要插入的项，splice\(2,0,'red'\)
* 替换：指定起始位置，要删除的项数和要插入的项，splice\(2,1,'red'\)

# 位置方法

indexOf，lastIndexOf

# 迭代方法

每个方法接收两个参数：要在每一项上运行的函数和（可选的）运行该函数的作用于对象——影响this。函数接收三个参数：数组项的值，该项在数组中的位置和数组本身

* every：对每一项运行函数，函数每一项都返回true，则返回true
* filter：对每一项运行函数，返回函数会返回true的项组成的数组
* forEach：对每一项运行函数，没有返回值
* map：对每一项运行函数，返回每次调用的结果组成的数组
* some：对每一项运行函数，如果有一个返回true，则返回true

# 缩小方法

reduce，reduceRight，返回一个值。方法接收两个参数，要在每一项上调用和函数和（可选的）作为缩小基础的初始值。函数接收四个参数：前一个值、当前值、项的索引和数组对象，函数的返回值会自动作为第一个参数传递给下一项，第一次迭代发生在第二项上

