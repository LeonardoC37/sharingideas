### Test 3 (Week 13)

一、选择题（回忆相关概念及知识点理解）：

1、在一个被调用函数中，关于return 语句使用的描述，错误的是

A. 被调用函数中可以不用return语句

B. 被调用函数中可以使用多个return语句

C. 被调用函数中,如果有返回值，就一定要有return语句

D. 被调用函数中,一个return语句可以返回多个值给调用函数 



2、若已定义``char s[10];``则在下面表达式中不表示``s[1]``的地址的是

A. s+1

B.s++

C. &s[0]+1

D. &s[1]



3、一个函数为``void f(int,float='a')``，另一个函数为``void f(int)``，则它们

A. 不能在同一个程序中定义

B. 可以在同一个程序中定义并可重载

C. 可以在同一个程序中定义，但不可重载

D. 以上说法均不正确



4、以下存储类标识符中，要求通过函数来实现一种不太复杂的功能，并且要求加快执行速度，应选用

A.内联函数

B.重载函数

C.递归调用

D.嵌套调用



二、阅读程序（考试题目中看程序写运行结果）：

```c++
1.
#include <iostream>
using namespace std;
class Point {
 	 int x, y;
public:
     Point() : x(0), y(0) {
     cout<<"Default"<<x <<endl;}
     Point(int x, int y) : x(x), y(y) {
     cout<< "C"<<x ; } 
     ~Point() { cout<<"D"<< x ; }
};
Point p0;
Point* m(){
     Point p1(1,2);
     static Point p3(3,4);
     Point *ptr4 =new Point(4,5); 
     Point *ptr5 =new Point(5,6);
     cout << endl;
     delete ptr4; 
     return ptr5; 
}
int main(){ 
     Point* ptr =m();
     delete ptr;
     return 0; 
}

```



```c++
2.
#include <iostream> 
using namespace std; 
class A{
 	public: A(int aa){cout<< aa;};
};
class B:public A{
     int b; A a;
     public:
     	B(int bb):a(bb-2),A(bb+1),b(bb+2){
     		b = bb-4;
     		cout << b <<endl;
		}
};
int main(){ A a(3); B b(4); } 

```



```c++
3.
#include <iostream>
using namespace std;
class B0
{ 
    public: 
        virtual void display() { cout << "B0::display()" << endl; }
        B0() { cout << "B0 called."; };
        ~B0() { cout << "~B0 called."; };
};
class B1 : public B0
{   
    public:
        void display() { cout << "B1::display()" << endl; }
        B1() { cout << "B1 called."; };
        ~B1() { cout << "~B1 called."; };
};
class D1 : public B1
{ 
    public: 
        void display() { cout << "D1::display()" << endl; }
        D1() { cout << "D1 called."; };
        ~D1() { cout << "~D1 called."; };
};
void fun(B0 *ptr){ ptr->display(); }
int main()
{ 
    B0 b0, *p;
    D1 d1;
    p = &b0;
    fun(p);
    p = &d1;
    fun(p); 
}

```


三、编写程序（补充程序代码或编写程序）：

1.定义 Complex 复数类（基本是必考题）

支持 ：1）通过类的成员函数的方式实现两个复数相加；

 2）c 是 Complex 的对象，支持语句“``cout << c;``”，能以“a+bi”的形式输出 c 的值.



2.编写程序，声明基类 Shape，由它派生出 2 个派生类： Circle(圆形)、 Rectangle(矩形)。在 main()中分别建立 2 个派生类的对象，2 个图形的数据在定义对象时给定，并调用下面的 printArea 函数输出其面积.

```cpp
//输出面积的函数 
void printArea(const Shape &s) 
{cout<<s.area()<<endl;} //输出s的面积
```





