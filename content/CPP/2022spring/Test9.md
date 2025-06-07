### Test 9 (Week 15)

一、阅读程序，写出运行结果

```cpp
//1.
#include<iostream>
using namespace std;
class A{
	int x,y;
	public :
		A(){cout<<"in A's default constructor\n";f();}
		A(const A&){cout<<"in A's copy constructor\n";f();}
		~A(){cout<<"in A's destructor\n";}
		virtual void f(){cout<<"A::f()\n";}
		void g(){cout<<"A::g()\n";}
		void h(){f();g();}
};
class B: public A{
	int x,y;
	public :
		B(){cout<<"in B's default constructor\n";f();}
		B(const B&){cout<<"in B's copy constructor\n";f();}
		~B(){cout<<"in B's destructor\n";}
		void f(){cout<<"B::f()\n";}
		void g(){cout<<"B::g()\n";}
};
void func1(A x){
	x.f();
	x.g();
	x.h();
}
void func2(A &x){
	x.f();
	x.g();
	x.h();
}

int main(){
	cout<<"-----1-----"<<endl;
	A a;
	A *p = new B;
	cout<<"-----2-----"<<endl;
	func1(a);
	cout<<"-----3-----"<<endl;
	func1(*p);
	cout<<"-----4-----"<<endl;
	func2(a);
	cout<<"-----5-----"<<endl;
	func2(*p);
	cout<<"-----6-----"<<endl;
	delete p;
	cout<<"-----7-----"<<endl;
	return 0;
}


//2.
#include<iostream>
using namespace std;
class A{
	int x;
	public :
		A(int i){ 
		x = i;
		cout<<"A"<<i<<endl;
		}
};
class B: virtual public A{
	int y;
	public :
		B(int i):A(1){
			y = i;
			cout<<"B"<<i<<endl;
		}
};
class C: virtual public A{
	int z;
	public :
		C(int i):A(2){
			z = i;
			cout<<"C"<<i<<endl;
		}
};
class D: public C,public B{
	int m;
	public :
		D(int i,int j,int k):B(i),C(j),A(3){
			m = k;
			cout<<"D"<<i<<endl;
		}
};
int main(){
	D d(1,2,3);
}
```

二、编程题

1. 定义类模板Point，有两个坐标(x,y)，x和y的类型可以不同，坐标的数据类型可以是int、float,double类型. 具有获取坐标的成员函数getX和getY。

2. 已知Horse类是Pegasus类的父类，请你编写一段程序，通过动态绑定调用Fly方法，如果调用的对象是Horse的实例，则输出“我是一匹马，不会飞的马”，如果调用的对象是Pegasus的实例，则输出“Believe me I can fly”。

3. （这是十五周的练习题，补充了第三问）

   定义 Complex 复数类，支持

   1）通过类的成员函数的方式实现两个复数相加；

   2）c 是 Complex 的对象，支持语句“cout << c;”，能以“a+bi”的形式输出 c 的值；

   3）定义++操作为实数部分加一，请实现++c和c++功能。