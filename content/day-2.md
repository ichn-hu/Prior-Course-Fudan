# 2 Hello World

负责人：[@Pryest](https://github.com/Pryest/)

欢迎大家来到今天的课程。

在第一天的课程中我们学习了如何安装编程平台和设置编译环境。

今天，我们将在C语言程序的学习中迈出一大步，独立自主地写出第一份C语言程序——Hello world程序，并且通过这个程序了解到C语言程序的基本结构。

正如我们在第一天的课程中了解到的那样，我们编写的C语言程序本质上只是一些文本文件，同样的文本文件可以在不同的环境进行编译，达到同样的效果。

换句话说，开发平台的不同并不会影响正常学习。

在今天的课程中，我们使用Windows操作系统下的Dev-C++作为开发平台，这可能会导致一些操作上的差异，同学们可以下来自行研究或者询问助教。

[toc]

## Hello World程序

首先，我们来动手实现一下Hello world程序。

Hello world程序代码如下：

```c
#include<stdio.h>
int main(){
	printf("Hello world\n");
	return 0;
} 
/*这里是无意义的注释*/
```

打开Dev-C++后，点击左上角的文件菜单栏。

![HW图1](https://raw.githubusercontent.com/Pryest/img/master/HW1.jpg)

选择新建，点击源代码选项。

![HW图2](https://raw.githubusercontent.com/Pryest/img/master/HW2.jpg)

以上步骤也可使用快捷键Ctrl+N完成。

![HW图3](https://raw.githubusercontent.com/Pryest/img/master/HW3.jpg)

编程时可以点击菜单栏第二行第三个黄色按钮进行保存，或者使用快捷键Ctrl+S进行保存。

![HW图4](https://raw.githubusercontent.com/Pryest/img/master/HW4.jpg)

我们通常把C语言程序保存为.c后缀的文件，代表这是一个C语言文件。

某些编译器会按照后缀来对不同种类程序的关键词进行高亮，方便我们调试。

我们要编写的程序的目的是在屏幕上输出hello world字样，这最早是Brian Kernighan在《B语言基础》中使用的例程。后来他在编写《C语言基础》时延用了这个例子并当做第一个例程。

因为这个程序简单明了，后来我们很多编程语言的教材都将其沿用为第一个例程。

在开始编写程序前，一定要将输入法转为英文输入：中文的字符都是全角字符，编译器无法识别。

我们将书上的程序先原样誊写在我们新打开的这个文件中。

![HW图5](https://raw.githubusercontent.com/Pryest/img/master/HW5.jpg)

保存后，我们在菜单栏中找到编译运行选项，编译运行的快捷键为F11。

![HW图6](https://raw.githubusercontent.com/Pryest/img/master/HW6.jpg)

编译运行后，会弹出cmd界面，并显示”Hello world“字样。

![HW图7](https://raw.githubusercontent.com/Pryest/img/master/HW7.jpg)

如此，我们便完成了第一个C语言程序——Hello world程序的编写和运行。

接下来我们将逐行解读C语言程序。

```c
#include<stdio.h>
```

include语句让我们可以调用系统库以使用对应的系统函数，在此处我们调用的库为stdio.h，使用的库函数为printf。

在编译器的帮助下，我们可以很方便使用这些库中的库函数而不需关心更底层的设计。

以下是一些其他的include实例。

```c
#include<stdlib.h>
#include<math.h>
#include<string.h>
```

这些库我们在之后都会学到，这里不要求掌握！！！

```c
int main(){
    ....
}
```

这里我们对main函数进行声明，int代表整型，代表一个一定范围内的整数，这里的int表示我们这个函数的返回值为整型变量，换句话说我们会收到整数作为main()的值。main是函数名称。括号内无内容表示main函数不需要参数。

main函数是代码层面上程序开始的地方，因此每个C语言程序都需要有且仅有一个main函数。

今天稍晚点我们会稍微讲讲函数的基本内容，此处不理解也没有问题！！！

函数用大括号{}将函数体包裹起来，表示这些代码属于这个函数，是函数必要的组成部分。

```c
printf("Hello world\n");
```

这一句我们调用了库函数printf，这个语句可以用于在屏幕上输出信息。

双引号代表一个字符串常量：按顺序排列的一串字符就是字符串，常量代表这个字符串是一个固定的字符串，不会随程序运行发生改变。

字符串常量中的\n表示换行符，也就是俗称的回车。

整句语句的意思是：输出Hello world并换行。

```c
return 0;
```

我们通常用函数返回值来表达函数执行的结果。

main函数的返回值设置为0，代表函数正常结束。

假如程序执行中，若发现返回值是其他数值，我们就知道main函数内部出了问题，需要检查函数或者输入数据。

```c
/*这里是无意义的注释*/
```

最后是注释语句，C语言中一段用/* */包裹起来的语句被称为注释。

注释内容不会被编译，但给程序加注释是一个很好的习惯。

注释就像我们随手写下的笔记，一方面有助于我们自己回忆，另一方面也有助于其他人理解我们的代码。

目前我们面对的都是一些小型的任务，没必要添加过多的注释，那样反而会浪费我们的时间。

但未来面临较复杂的任务时（如下半学期的面向对象程序设计），注释有助于我们记忆阶段性的成果，避免无意义的重复劳动。



## C语言程序基本框架

```c
#include<库文件>
函数返回值类型 函数名(参数表){
    函数体
}
...
函数返回值类型 main(命令行参数){
	函数体
}
```

C语言写成的程序是由若干个（至少一个）函数组成的，其中必须有一个函数的函数名为main。

那么函数又是什么东西呢？

许多程序设计语言中，我们可以将一段经常需要使用的代码打包封装起来（比如说计算平方根或者绝对值），在需要使用时可以直接调用，这些封装起来的代码就是函数。

函数的格式一般为：

```c
函数返回值类型 函数名(参数表){
    函数体
}
```

当这个函数不需要参数时，小括号里的参数表可以为空。

以下是几个函数的例子：

```c
int sum(int a,int b){
    return a+b;
}
int sqr(int x){
    return x*x;
}
int zero(){
    return 0;
}
```



## A+B程序

```c
#include<stdio.h>
int main(){
	int a,b,sum;/*定义三个整型变量，相当于申请三个存放整数的单元*/ 
	scanf("%d%d",&a,&b);/*从键盘读入a和b的值*/ 
	sum=a+b;/*将a+b的值装入sum这个单元格*/ 
	printf("%d+%d=%d\n",a,b,sum);/*输出加法算式*/
	return 0;/*正常结束*/
	/*我们能否用sum函数代替某一步的某一部分？如果可以，是哪一部分*/ 
} 
```

借助注释，我们可以很轻松地理解这个程序，我们也很推荐同学们自己上手试试这个程序。

注意！！！这个程序有很多可以改进的地方，面对某些输入甚至会给出错误的答案，感兴趣的同学们可以自行探索。

大学学习不同于中学，更多的靠自主学习而非老师精细的教导。但自主学习的方法也很多，不管是上网查阅资料还是向老师助教提问都是很好的方法，但我们推荐的解决方法是：1.自主思考 2.查阅资料 3.向同学求助 4.向助教求助 5.向老师求助 6.向专业人士求助。



## 编译小贴士

在编程过程中，有的时候编译器无法成功完成自己的工作，这是因为我们的代码中有一些错误。

1. 如果编译失败，看看是不是有语句后面缺少分号。

2. 如果还是失败，看看是不是有中文符号。

   例如： （应改为(  ;应改为;  ）应改为)

3. 如果再失败，读一读编译信息，看看问题出在哪一行，看看如何改正。

4. include语句必须放在代码的最前端。



## 课后练习

1. 第二天 Hello world 程序章节的课后作业

2. OJ上可能会有一些简单的输入输出练习。
