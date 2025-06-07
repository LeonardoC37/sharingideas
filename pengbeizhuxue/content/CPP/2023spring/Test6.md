### Test 6(Week 16)

一、选择题（回忆相关概念及知识点理解）：

1、若 x=4，则 x*=x+2 的值为:

A. 36 

B. 24 

C. 18 

D. 20 



2、在函数定义前加上关键字“inline”表示该函数被定义为: 

A. 重载函数 

B. 内联函数 

C. 成员函数 

D. 普通函数 

二、阅读程序（考试题目中看程序写运行结果）：

```c++
#include <iostream>
using namespace std;

class A{
    int a;
    public:
        A() : A(0){}
        A(int i):a(i) { cout << a; };
};
class B:public A{
    A a1,a2;
    int b;
    public:
        B(int i):A(i+1),a1(i+2),a2(),b(i){
        cout << b <<endl;
    }
};
int main(){ A a(6); B b(6);}
```





三、编写程序（补充程序代码或编写程序）：

1.公交刷卡播报场景仿真：乘坐公交的人可能是老师、学生，也可能 是工人、农民或者某个程序员。请通过类的继承，完善类 Human、 Teacher 和 Student。在 main 函数中模拟上车买票的场景，车上上来两个人，一个是老 师，另一个是学生，调用普通函数 GetOn 两次，分别输出“老师投币买票”、“学生刷 卡买票”。 





```c++
class Human // 定义 Human 类
{ public:
 _______________________________// 1、买票接口函数
 { cout<<"人买票。"<<endl; }
};
class Teacher ___________________________ //2、派生老师类
{ public:
 void BuyTicket()
 { cout<<"老师投币买票。"<<endl; }
};
class Student_____________________________//3、派生学生类
{public:
 void BuyTicket()
 { cout<<"学生刷卡买票。"<<endl; }
};
void GetOn(Human *h)
{ 
____________________________________; //4、调用 BuyTicket
}
int main() // 主函数中模拟上车买票的场景，车上上来两个人，一个是老师，另一个是学生
{ 
Teacher * pt = new Teacher();
 Student * ps = new Student();
GetOn(pt); // 第一个人是老师，投币买票
GetOn(ps); // 第二个人是学生，刷卡买票
________________________________________; // 5、销毁对象
return 0;
}
```