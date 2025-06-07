### Test 5(Week 15)

一、选择题（回忆相关概念及知识点理解）：

1、对于如下定义：int k, a[10],\* p=a; 哪个表达式是不对的 

A.\* p++=2

B.p++

C.a++

D.a[0]=k  



2、以下说法中正确的是： 

A. 一个类一定会有无参构造函数

B.构造函数的返回值类型是 void 

C. 一个类只能定义一个构造函数, 但可以定义多个析构函数

D. 一个类只能定义一个析构函数，但可以定义多个构造函数 



二、阅读程序（考试题目中看程序写运行结果）：

```c++
#include <iostream>
using namespace std;

class Obj {
public:
    Obj(){
        count++;
        cout <<"obj "<< count << "remain" << endl;
    }
    ~Obj(){
        count--;
        cout <<"Obj " << count <<"left"<< endl;
    }
    static int count;
};
int Obj::count = 0;
int main(){
    Obj c1;
    Obj *p = new Obj();
    delete p;
    Obj c2(c1); 
    //提示，此处调用缺省复制构造函数
    return 0;
}
```



三、编写程序（补充程序代码或编写程序）：

1.定义类模板 Point，有两个坐标(x,y)，私有成员 x 和 y 的类型可以 不同，坐标的数据类型可以是 int、float, double 类型. 具有获取 坐标的成员函数 getX 和 getY，支持如下使用

```cpp
Point<int,int> p1(10, 20); 
Point<int,float> p2(10, 20.5f); 
cout<<p1.getX()<<","<<p1.getY()<<endl;
cout<<p2.getX()<<","<<p2.getY()<<endl;
```

