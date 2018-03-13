# 2019.3.13

#### 填空

null+1 // 1  
undefined+1    // NaN  
typeof NaN     // 'Number'  
typeof 4\*_'a'     // 'NaN'  _typeof优先级高于+-\*/低于括号  所以顺序是typeof 4返回'number'再乘'a'返回'NaN'  
typeof \(4\*'a'\)  // 'Number'

