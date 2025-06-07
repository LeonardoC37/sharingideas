### Test 1 (Week 7)


一、选择题

1. 编写C++程序一般需经过的几个步骤依次是

    A. 编辑、调试、编译、连接

    B. 编辑、编译、连接、运行

    C. 编译、调试、编辑、连接

    D. 编译、编辑、连接、运行



2. 下面哪个是c++合法的标识符

    A.friend   B.1car    C.Car   D.No.1    E.PI



3. 下列说法错误的是

    A.if(a&1)可以用于判断a是否为奇数

    B.逻辑与&&的优先级比逻辑或||高

    C.int a=1;if(true || a++) cout<<a;程序输出结果为2

    D.cout<<(1==2==3)<<" "<<(1<3<2);输出结果为0 1



4. 下列关于类型转换的说法中，正确的一项是

    A、double可以隐式类型转换为int类型

    B、double类型可以隐式类型转换为int类型

    C、double类型只能显示类型转换为int和long类型

    D、double类型可以显示类型转换为bool类型



5. 以下不能正确进行字符串赋初值的语句是

    A. char str[5]=”good!”; B. char str[]=”good!”;

    C. char *str=”good!”;  D. char str[5]={‘g’,’o’,’o’,’d’};



6. 下列说法错误的是

    A. unsigned int表示无符号数，与int相比其内存空间中没有表示符号的位

    B. 全局变量的标记符为const，静态变量为static

    C. sizeof() 是一种内存容量度量函数，功能是返回一个变量或者类型的大小

    D. 整数类型字面常量由0x开头表示的是八进制，而32765L表示的是其为long int型字面常量



二、 阅读程序，写出运行结果

```C++
1. #include<bits/stdc++.h>
using namespace std;
int main(){
    int a=1,b=5;
    cout<++a<<" "<<b--<<endl;
    cout<<a%b<<endl;
    a*=(--b);
    cout<< a ;
}
```



```c++
2. #include<bits/stdct+.h>
using namespace std;
int main()｛
    int a=1314,i=0;
    char sentence[]= "dream team!";
    while(a>>=1){
        if (sentence[i]>=65 &&sentence [i] <= 122)
            cout<< (char) (sentence[i++]-32);
        else{
            cout<<"*";
            i++;
        };
    }
}
```



三、编程题

1. 用递归函数实现斐波那契数的计算

$$
fib(n)=\left\{ \begin{matrix}
1,n=1  \\
1,n=2  \\
fib(n-2)+fib(n-1),n\ge 3  \\
\end{matrix} \right.
$$




2. 用尽可能快的方法实现求解200以内所有素数并输出。