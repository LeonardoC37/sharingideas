### Test 4 (Week 14)

一、选择题（回忆相关概念及知识点理解）：

1、语句 ``cout << 'C' << 'C'+32;`` 输出的结果是： 

A. CC32 

B. Cc 

C. 6799 

D. C99 



2、关于 C++函数的下列描述，正确的是： 

A. 有些函数定义即使加上了 inline 关键词，编译程序也不会把它作为内联函数来对待； 

B. 函数 `void f(int a){}` 与 `void f(int b=10){}` 是重载关系；

C. `void f(){ void g();}`是在函数 f()内部嵌套的定义了另一个函数 g()； 

D. 假设有宏定义`#define max(a,b) a>b?a:b`，则 `cout<<max(2+2,3);`的结果是4.



3、不正确的表述是：

A. 基类中的纯虚函数只有定义，没有实现 

B. 如果一个类中包含没有实现的纯虚函数的类，则不能用这个类创建对象 

C. 纯虚函数应当是非 private 成员函数

D. 一个类中，如果有 virtual 修饰的函数，则这个类是抽象类 



4、如果限制 a.cpp 中的函数 f()不能在其他 cpp 文件中被直接调用，则应该在 f 前面添加关键字：

A. private 

B. static 

C. extern 

D. const



二、阅读程序（考试题目中看程序写运行结果）：

```c++
1.
int main(){
    int a = 3, b = 4;
    int *p1=&a, *p2=&b;
    p1=&a; p2=&b;
    cout << a << b << endl;
    if (a<b){
    	int* p=p1; p1=p2; p2=p;
    }
    cout << a << b << endl;
    cout<<*p1<<*p2<<endl;
}

```



```c++
2.
int a[] = {0 ,1, 2, 3};
int &b = a[1];
int *p = &b;
cout << a[3] << endl;
cout << b++ ;
cout << *p++ << endl;
cout << *p << *(p+1) << endl;

```



```c++
3．
#include "iostream"
using namespace std;
int main(void)
{ 
    int a[6], i;
 	for (i=1; i<6; i++)
 	{ 
        a[i]=9*(i-2+4*(i>3))%5 ;
 		cout<<a[i]<<'\t';
 	}
}
```



三、编写程序（补充程序代码或编写程序）：

1.用递归方法求 n 阶勒让德多项式的值,递归公式为 ：


2.编写程序输出 100 到 200 之间的所有素数。（所谓素数是指除了 1 和它本身外，不能 被其他数所整除的数） .