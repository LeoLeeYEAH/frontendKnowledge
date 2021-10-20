### ECMAScript 6 新特性

阮一峰的官方教材非常详尽的介绍了ES6的新特性：https://es6.ruanyifeng.com/ 本文仅对一些常用的新特性进行归纳总结

+ 新增了let和const两个变量，引入了块级作用域的概念，同时let还具有不存在变量提升、会触发临时性死区、不能重复定义等特点

+ 新增了Symbol数据类型，用以生成一个独一无二的值

+ 新增了Set和Map两个数据结构

+ 新增了Promise对象用以解决异步编程，详情可以参考 [Promise](Promise相关.md)

+ 添加了`for...in`和`for...of`两种新的for遍历方法

+ 引入了Class的概念，通过class关键字，可以直接进行类的定义

+ 字符串方法的扩展
    + 新增了数个String对象方法，包括：includes / replaceAll / trimStart / trimEnd / startsWith / endsWith 等

+ 数值方法的扩展，
    + 新增了数个Number对象方法，包括：parseInt / parseFloat / isInteger / isFinite / isNaN 等
    + Math对象的扩展
        + trunc 去除一个数的小数部分
        + sign 判断一个数是正数、负数、还是零
        + cbrt 计算一个数的立方根
        + log2 / log10 等对数方法
    + 新增了BigInt数据类型，BigInt只用来表示整数，没有位数的限制，任何位数的整数都可以精确表示

+ 数组的扩展
    + 新增了扩展运算符`...`，可以将将一个数组转为用逗号分隔的参数序列，使用举例：`Math.max(...arr)` `arr1.push(...arr2)` `let [...arr2] = arr1`
    + 新增了Array.from方法，用于将类似数组的对象和可遍历的对象转为真正的数组
    + 新增了find和findIndex方法，用于找出第一个符合条件的数组成员，它的参数是一个回调函数
    + 此外还新增了 fill / includes / flat 等方法

+ 函数的扩展
    + 可以为函数的参数设置默认值
    + 箭头函数
    
+ 模块语法的引入
    + 新增了import关键字取代require()
    + 新增了export关键字取代module.exports





