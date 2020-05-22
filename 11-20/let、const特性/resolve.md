const 是块级作用域
第一个循环中，数组 push 的是不同的对象，结果为[{name: ‘a’},{name: ‘b’},{name: 'c’}]；第二个循环中，数组 push 的同一个对象，循环最后变成[{name: ‘c’},{name: ‘c’},{name: 'c’}]
