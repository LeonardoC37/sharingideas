### Test 7 (Week 13)

一、阅读程序，写出运行结果

```cpp
//1.
#include <iostream>
using namespace std;
class Circle{
	private : double x, y, r,count;
	public: 
	Circle(int count){
		x = 1,y = 1,r = 1;
		this->count = count;
	}
	Circle(double x,double y,double r,int count){
		this->x = x;
		this->y = y;
		this->r = r;
		this->count = count;
	}
	~Circle(){
		cout<<"D"<<count<<endl;
	}
};
static Circle c1(1);
Circle c2(2,2,2,2); 
Circle* dosomethings(){
	Circle *c3 = new Circle(3);
	static Circle c4(1,1,1,4);
	Circle c5(5);
	return c3;
} 
int main(){
	Circle *c6 = dosomethings();
	delete c6;
}

//2.
#include <iostream>
using namespace std;
class B{
public:
    B(){
        cout << "B:B() is called" << endl;
    }
    B(int x){
        cout << "B:B(x) is called" << endl;
        x = a;
    }
private:
    int a;
};
class A{
public:
    A(int x){
        a = x;
        b = B(x);
        cout << "A:A() is called" << endl;
    }
    ~A() {}
private:
    int a;
    B b;
};
int main(){
    A t(1);
    return 0;
}
```

二、编程题

定义 Complex 复数类，支持

1）通过类的成员函数的方式实现两个复数相加；

2）c 是 Complex 的对象，支持语句“``cout << c;``”，能以“a+bi”的形式输出 c 的值；