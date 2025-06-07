### Test 6 (Week 12)

一、单选题

1. 对类的构造函数和析构函数描述正确的

   A.构造函数可以重载，析构函数不能重载

   B.构造函数不能重载，析构函数可以重载

   C.构造函数可以重载，析构函数也可以重载

   D、构造函数不能重载，析构函数也不能重载

 

2. 下面对静态数据成员的描述中，正确的是

   A.静态数据成员可以在类体内进行初始化

   B.静态数据成员不可以在类体内进行初始化

   C.静态数据成员不能受private控制符的作用

   D.静态数据成员可以直接用类名调用

 

3. 在程序代码:``A::A(int a, int *b) { this->x = a; this->y = b;}``中,this的类型是

    A. int

    B. int *

    C.A

    D.A*

 

4. 如果类A被说明成类B的友元，则

   A、类B同样也是类A的友元

   B、类B的成员即类A的成员

   C、类A的成员函数不能访问类B的成员

   D、类A的成员函数可以访问类B的成员

5. 关于友元的描述中，错误的是

   A．友元函数是成员函数，它被说明在类体内

   B．友元函数可直接访问类中的私有成员

   C．友元函数破坏封装性，使用时尽量少用

   D．友元类中的所有成员函数都是友元函数

   

6. 设有定义:

   ```cpp
   class person{ int num;char name[10];public:
   void init(int n,char *m) ;
   person std[30];
   ```

   则以下叙述不正确的是()

   A. std是一个含有3 0个元素的对象数组

   B. std数组中的每一个元素都是person类的对象

   C. std数组中的每一个元素都有自己的私有变量num和 name

   D. std数组中的每一个元素都有各自的成员函数init

 

二、阅读程序，写出运行结果

```cpp
#include <iostream>
using namespace std;
class point{
    int x, y;
    public:
    point(int a, int b){
        x=a; y=b;
        cout<<"calling the constructor function."<<endl;
    }
    point(point &p);
    friend point move(point q);
    ~point() {cout<<"calling the destructor function.\n";
             }
    int getx() {return x;}
    int gety() {return y;}
};
point::point(point &p){
    x=p.x ;y=p.y;
    cout<<" calling the copy_initialization constructor function. \n";
}
point move(point q){
    cout<<"OK ! \n";int i, j;
    i=q.x+10;j=q.y+20;point r(i, j);
    return r;
}
int main(){
    point m(15,40), p(0,0);
    point n(m);
    p=move (n);
    cout<<"p="<<p.getx ()<<","<<p. gety ()<<endl;
} 
```

三、编程题

1. 定义一个类A，使得在程序中只能创建一个该类的对象，当试图创建该类的第二个时，返回第一个对象的指针。

2. 编写一个时间类（数据成员只含小时和分钟），支持两个时间用“+”相加。

 