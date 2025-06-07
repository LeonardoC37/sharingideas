### Test 2 (Week 12)

一、选择题（回忆相关概念及知识点理解）：

1、在 C++中，源程序编译可执行程序的正确顺序应该是： 

A. 编辑、链接、编译、执行 

B. 编辑、编译、链接、执行 

C. 编译、编辑、链接、执行

 D. 编译、链接、编辑、执行 



2、设有如下定义： ``char *aa[2]={"abcd", "ABCD"}; ``则以下说法中正确的是:  

A. aa 数组中的元素值分别为"abcd"和"ABCD"

B. aa 是指针变量，它指向含有两个数组元素的字符型一维数组

C. aa 数组的两个元素分别存放的是含有 4 个字符的一维字符数组的首地址 

D. aa 数组的两个元素中各自存放了字符'a'和'A'的地址 



3、设有以下说明语句： ``struct ex { int x ; float y; char z ;} example;`` 则下面的叙述中不正确的是: 

A．``struct`` 是声明结构体类型的关键字 

B．``example`` 是结构体类型名 

C．``x,y,z`` 都是结构体成员名 

D．``struct ex`` 是结构体类型 



4、下面对类中静态数据成员的描述中,正确的是： 

A. 静态数据成员是类的所有对象共享的数据 

B. 类的每个对象都有自己的静态数据成员 

C. 类的不同对象有不同的静态数据成员 

D. 静态数据成员不能通过类的对象访问 



5、已知类 A 中的一个成员函数的说明如下：``void Set(A &a);``则该函数的参数“``A &a``” 的含义是( )。 

A. 指向 A 的指针为 a 

B. 将变量 a 的地址赋给类 A 

C. 类 A 对象引用 a 用作函数的形参 

D. 变量 A 与 a 按位与后作函数参数 



二、阅读程序（考试题目中看程序写运行结果）：

```c++
1.
int a[] = {5, 4, 3, 2, 1};
int *p = a + 1;
cout << *p << p[1];
cout << *p++;
(*p)++;
cout << *(a+2)<<*(p+2)<<*p+2;
```





```c++
2.
#include <iostream>
using namespace std;
int fun(int x)
{
 if (x <= 0)
 {
 	return 0;
 }
 else
 	return x * x + fun(x - 1);
}
int main()
{
 	int x = fun(3);
 	cout << x << endl;
 	return 0;
}

```



```c++
3.
void change(char *pchar)
{ 
   while(*pchar)
  { 
       if(*pchar>='A' && *pchar<='Z')
     		*pchar=*pchar+32;
       pchar++;
       if(*pchar==0) break;
       pchar++;

  }
}
char cc[]={"886CPP"};
change(&cc[1]);
cout <<cc<<endl;
```



三、编写程序（补充程序代码或编写程序）：

1.下面程判断输入的字符串是否"回文"（前后对称），忽略字符串前后的空 格。若是回文，输出 YES 

```c++
#include <iostream>
#include <string.h>
using namespace std;
int main(void)
{ char s[81], cr, *pi, *pj;
 int i, j, n;
 cin.getline(s,80); n=strlen(s);
 pi=________; pj=________;//pi 指向串开始，pj 指向最后
 while(*pi==' ') ________;
 while(*pj==' ') ________;
 while( ( ________) &&(*pi==*pj) )
 { pi++; pj--; }
 if(pi<pj) cout<<"NO"<<endl;
 else cout<<"YES\n";
}

```

2.定义两个重载函数 mod，分别求两个整数相除的余数和两个实数相除的余数。两个实数求余定义为实数四舍五入取整后相除的余数。 在 main 函数中调用这 2 个 mod 函数，写出完整的可以编译运行的程序。 