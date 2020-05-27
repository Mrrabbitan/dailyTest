回调函数

官方定义：A callback is a function that is passed as an argument to another function and is executed after its parent function has completed.
定义：js 中函数是一个引用数据类型，所以我们传入的不可能是一个函数，而是函数的指针。所以这里应该是先定义好函数，然后把指针作为参数传递给调用它的函数
解决的问题：最常遇到的一个是事件处理函数，一个是异步请求的数据处理函数。异步请求的回调函数，相似的处理，也是将数据处理的部分单独封装，在数据返回之后调用

优点：优点前面提到了，高内聚低耦合，减少重复代码，提高可读性

缺点：回调造成一个代码的嵌套，层级多了就是回调地狱. Callback Hell
