1. 调用 ES6 中的 flat 方法

ary = ary.flat(Infinity);
复制代码

2. replace + split

ary = str.replace(/(\[|\])/g, '').split(',')
复制代码

3. replace + JSON.parse

str = str.replace(/(\[|\])/g, '');
str = '[' + str + ']';
ary = JSON.parse(str);

4. 普通递归

let result = [];
let fn = function(ary) {
for(let i = 0; i < ary.length; i++) {
let item = ary[i];
if (Array.isArray(ary[i])){
fn(item);
} else {
result.push(item);
}
}
}
复制代码

5. 利用 reduce 函数迭代

function flatten(ary) {
return ary.reduce((pre, cur) => {
return pre.concat(Array.isArray(cur) ? flatten(cur) : cur);
}, []);
}
let ary = [1, 2, [3, 4], [5, [6, 7]]]
console.log(flatten(ary))
复制代码
6：扩展运算符

//只要有一个元素有数组，那么循环继续
while (ary.some(Array.isArray)) {
ary = [].concat(...ary);
