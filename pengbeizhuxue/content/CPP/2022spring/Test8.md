### Test 8 (Week 14)


一、阅读程序，写出运行结果

```cpp
//1.
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
int main(){
    A a(3);
    B b(4);
}


//2.
#include <iostream>
using namespace std;
class B0{
    public:
    virtual void display() { cout << "B0::display()" << endl; }
    B0() { cout << "B0 called.\n"; };
    ~B0() { cout << "~B0 called.\n"; };
};
class B1 : public B0{
    public:
    void display() { cout << "B1::display()" << endl; }
    B1() { cout << "B1 called.\n"; };
    ~B1() { cout << "~B1 called.\n"; };
};
class D1 : public B1{
    public:
    void display() { cout << "D1::display()" << endl; }
    D1() { cout << "D1 called.\n"; };
    ~D1() { cout << "~D1 called.\n"; };
};
void fun(B0 *ptr){ ptr->display(); }
int main(){
    B0 b0, *p;
    D1 d1;
    p = &b0;
    fun(p);
    p = &d1;
    fun(p);
}
```





二、编程题

编写程序，声明基类 Shape，由它派生出 2 个派生类： Circle(圆形)、Rectangle(矩形)。在 main()中分别建立 2 个派生类的对象，2 个图形的数据在定义对象时给定，并调用下面的 printArea 函数输出其面积。

```cpp
//输出面积的函数
void printArea(const Shape &s)
{cout<<s.area()<<endl;} //输出 s 的面积
```