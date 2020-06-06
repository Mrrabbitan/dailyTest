解析：

函数接收两个参数，hobbies 有着默认值 person.hobbies，首先调用 addHobby，并给 hobby 传递 running，给 hobbies 传递一个空数组，因为我们给 hobbies 传递了空数组，running 被添加到空数组中。

第二项调用 addHobby 方法，并给 hobby 传递 dancing，我们不响 hobbies 传值，因此 hobbies 使用默认值 person 的 hobbies，因此我们想 person.hobbies 中 push 进去 dancing

第三项调用后并向 hobby 传值 playingGames，向 hobbies 传值修改后的 person.hobbies.因此最终返回为

["coding", "debug", "dancing", "playingGames”]
