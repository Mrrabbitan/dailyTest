答案：1、2、3. promise{<pendng>}

例一：首先在函数 range 中我们在遍历的过程中会生成 end-start+1 个 Promise 对象，之后在立即执行函数中会将生成的 async object promise 数组赋值给 gen，在 for 循环遍历后返回三个 promise，又因为我们在立即执行函数中，因此返回 resolved 的值 1、2、3

例二：在异步函数中始终返回一个 promise，await 后始终需要等待 promise 的执行结果，当赋值给 data 后，data 依然是返回一个 pending 状态的 promise，仍未得到执行结果。假如需要获得其执行结果，我们可以在 data 后加上.then 方法，或者模仿例一将 getData

函数放入立即执行函数中
