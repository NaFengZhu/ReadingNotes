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

－－－－－－－－－－－－－－－ Data Class  －－－－－－－－－－－

10.Data class 要求

```
1.primary 构造函数至少需要一个参数

2.所有primary 构造函数必须用val or var 来表示

3.Data class不能被abstrct inner open sealed修饰

4.Data class 不能继承其它的类，但是可以实现接口
```

11.Kotlin提供了标准的Data class对象，但是自定义data class 对象是更好的选择，因为对于项目来说自定义更有意义

```
标准的库提供了 Pair 和 Triple
```

－－－－－－－－－－－－－－－ Data Class －－－－－－－－－－－

－－－－－－－－－－－－－－－ Destructuring Declaration －－－－－－－－－－－

12.把一个对象分解为一些不同变量 这种语法叫Destructuring Declaration

－－－－－－－－－－－－－－－ Destructuring Declaration －－－－－－－－－－－

13.修饰符

```
1.private 它表示只能被自己所在的文件看见
```

14.什么是model

![](/assets/3.png)

15.在lambda中，最后一行表示返回值。你不需要使用 return关键字（实际上不能被编译）

16.not Null 分类

```
1.第一种情况是使用可空类型并且赋值为null,直到我们有了真正想赋的值。但是我们就需要在每个地方不管是否为null都要去检查。如果我们确定这个属性在任何我们使用的时候都不会是null,这可能需使得我们要编写一些必要的代码

2.第二种情况是使用 notnull委托，它会含有一个可null的变量并会在我们设置这个属性的时候分配一个真实的值。如果这个值在被获取之前没有被分配，它就会抛出一个异常
```

17.函数式编程的意义

```
函数式编程很不错的一点就是我们不用去解释我们怎么去做，而是直接说我想做什么。比如，如果我想去过滤一个list,不用去创建一个list ,遍历这个list 的每一项，然后如果满足一定的条件的时候放到一个新的集合中，而是直接使用filer函数并指明我想用的过滤器。用这种方式，我们可以节省大量的代码
```

18.可null类型怎么工作

```
1.我们确定我们是在用一个非null变量，如果变量类型是可null的，我们可以使用！！操作符来“强制”编译器执行可null类型时跳过限制检查。但是有可能会导致崩溃。如果一份代码满篇都是!!，那就有股代码没有被正确处理的味道了
```

19.可null性和Java库

```
当我们去处理Android SDK时，你可能看见所有Java 方法参数被标记为单个！。比如，Java中在一些获取对象的方法在Kotlin中显示返回Any!, 这表示让开发者自己决定这个变量是否可null。很幸运，新版本的Android SDK开始使用注解来辨别参数是否可null
```

20.但是没有什么是不能通过扩展函数来解决的

21.![](/assets/4.png)

22.When 表达式

```
when表达式于Java中的Switch\/case类似，但是要强大的多。与Java中Switch\/case不同的地方是参数可以是任何类型，并且分支也可以是一个条件
```

![](/assets/5.png)

![](/assets/6.png)

23.For循环

![](/assets/7.png)

24.

