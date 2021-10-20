### Promise对象

阮一峰的官方教材非常详尽的介绍了Promise对象：https://es6.ruanyifeng.com/#docs/promise 本文仅对一些基础的Promise对象知识点进行归纳总结

+ 什么是Promise对象
<br>Promise是异步编程的一种解决方案，比传统的解决方案更合理和更强大，Promise简单来说就是一个容器，里面保存着某个未来才会结束的事件的结果，Promise提供统一的API，各种异步操作都可以用同样的方法进行处理。

+ Promise的特点
    + Promise的状态不受外界影响。Promise有三种状态：**pending**、**fulfilled**和**rejected**，只有异步操作的结果，可以决定当前是哪一种状态，任何其他操作都无法改变这个状态。
    + Promise的状态一旦改变就不会再变。Promise对象的状态改变，只有两种可能：**pending** ==> **fulfilled** 和 **pending** ==> **rejected**，只要这两种情况发生，状态就不会再变了，这时就称为**resolved**。
    + 有了Promise对象，就可以将异步操作以同步操作的流程表达出来，避免了层层嵌套的“回调地狱”。此外，Promise对象提供统一的接口，使得控制异步操作更加容易。

+ Promise的不足
    + Promise一旦新建就会立即执行，无法中途取消。
    + Promise内部抛出的错误，不会反应到外部，因此必须设置回调函数。
    + Promise处于pending状态时，无法得知目前进展到哪一个阶段。

+ Promise.all()
<br>const p = new Promise([p1, p2, p3])，p的状态由p1、p2、p3决定，分成两种情况：
    + 只有p1、p2、p3的状态都变成fulfilled，p的状态才会变成fulfilled，此时p1、p2、p3的返回值组成一个数组，传递给p的回调函数。
    + 只要p1、p2、p3之中有一个被rejected，p的状态就变成rejected，此时第一个被reject的实例的返回值，传递给p的回调函数。

+ Promise.race()
<br>const p = new Promise.race([p1, p2, p3])，p的状态由p1、p2、p3决定：只要p1、p2、p3之中有一个实例率先改变状态，p的状态就跟着改变，率先改变状态的Promise实例的返回值，传递给p的回调函数。  

+ Promise.allSettled()
<br>const p = new Promise([p1, p2, p3])，不管是p1、p2、p3的状态是fulfilled或rejected，只有等到参数数组的所有Promise对象都发生状态变更，返回的Promise对象才会发生状态变更。

+ Promise.any()
<br>any()方法与all()方法正好相反：参数数组中有一个变成fulfilled状态时，包装实例就会变成fulfilled状态；而只有参数实例都变成rejected状态，包装实例才会变成rejected状态。


