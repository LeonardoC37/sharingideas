### Test 5 (Week 11)

一、单选题

1. 下面对类中静态数据成员的描述中,正确的是

    A. 静态数据成员是类的所有对象共享的数据

    B. 类的每个对象都有自己的静态数据成员

    C. 类的不同对象有不同的静态数据成员

    D. 静态数据成员不能通过类的对象访问

2. 下列for循环的次数为

   ``for(i=0，x=0; !x&&i<=5; i++)``

    A.5

    B.6

    C.1

    D.无限

3. 在一个被调用函数中，关于return 语句使用的描述，错误的是

    A.被调用函数中可以不用return语句

    B.被调用函数中可以使用多个return语句

    C.被调用函数中,如果有返回值，就一定要有return语句

    D.被调用函数中,一个return语句可以返回多个值给调用函数



4. 以下哪项不是构造函数的特征

    A.构造函数的函数名与类名相同

    B.构造函数可以重载

    C.构造函数可以设置缺省参数

    D.构造函数必须指定类型说明

5. 在如下结构定义中,不正确的是

    A.

    ```cpp
    struct student
    {int no;char name[10];float score;};
    ```

    B.

    ```cpp
    struct stud[20]
    {int no;char name [10];float score;};
    ```

    C.

    ```cpp
    struct student
    {int no;char name[10];float score;} stud[20];
    ```
    D.

    ```cpp
    struct
    {int no;char name[10];float score;} stud[100];
    ```

6. 已知: ``print ( )``函数是一个类的常成员函数,它无返回值，下列表示中，正确的是

    A. void print( ) const;

    B.const void print ( );

    C.void const print();

    D.void print(const);

二、阅读程序，写出运行结果

1. 阅读程序，写出运行结果

    ```cpp
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

2. 阅读程序，写出运行结果


    ```CPP
    #include <iostream> 
    using namespace std; 
    class A{
        public: A(int aa){cout<< aa;};
    };
    class B{
        int b; A a;
        public:
        B(int bb):a(bb-2),b(bb+2){
            b = bb-4;
            cout << b <<endl;
        }
    };
    int main(){ 
        A a(3); B b(4); 
    }
    ```