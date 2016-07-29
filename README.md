# Kotlin for android developer 笔记

1.类继承，Kotlin里的类默认是不能被继承的，只有哪些生命了open 和 abstrct 的类才能被继承

2.Kotlin构造函数的函数体是  init {... }

3.Unit是跟Java中的void类似，但是Unit是一个真正的对象

4.Kotlin中一切都是对象，不像Java中还包含一些基本类型

5.基本类型

```
1.数字类型不会自动转型

2.字符不能自动转换为数字

3.运算符也有一部分不一样

    ![](/assets/1.png)

4.一个字符串可以像数组那样被访问，迭代
```

6.一个重要的概念：尽量使用val

7.执行一个请求

![](/assets/2.png)

8.`AsyncTasks`会非常危险，因为当运行到`postExecute`时，如果Activity已经被销毁了，这里就会崩溃。

9.**一切kotlin函数都会返回一个值**

