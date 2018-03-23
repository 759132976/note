# 迭代器

迭代器是一种特殊的对象，每个迭代器对象都有一个next\(\)方法，每次调用返回一个结果对象。对象有两个属性：value，表示下一个要返回的值；done，当没有更多数据返回的时候返回true。若在最后一个值之后调用next\(\)方法会返回{value:undefined,done:true}

# 生成器

* 生成器用来生成迭代器，在function关键字之后加\*来表示：function \*createIterator\(\){}



