单纯的函数调用走 apply 方法，new 一个实例走 constructor,后两个走 get 方法
在 proxy 中
get 方法用于拦截某个属性的读取操作，可以接受三个参数，依次为目标对象、属性名和 proxy 实例本身
apply 方法拦截函数的调用、call 和 apply 操作。apply 方法可以接受三个参数，分别是目标对象、目标对象的上下文对象（this）和目标对象的参数数组
construct 方法用于拦截 new 命令，接收三个参数。

- target：目标对象
- args：构造函数的参数对象
- newTarget：创造实例对象时，new 命令作用的构造函数（下面例子的 p）
