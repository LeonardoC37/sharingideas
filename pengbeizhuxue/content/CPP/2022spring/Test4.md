### Test 4 (Week 10)

一、单选题

1. 已知类 A 中的一个成员函数的说明如下：``void Set(A &a);``则该函数的参数“``A &a``”的含义是( )。

    A. 指向 A 的指针为 a

    B. 将变量 a 的地址赋给类 A

    C. 类 A 对象引用 a 用作函数的形参

    D. 变量 A 与 a 按位与后作函数参数


2. 当把一个一维数组传给一个函数时，编译器会把数组变量a类型转换为？

    ```cpp
    void f(int p[],int num);
    int main(){ int a[10]; f(a,10);}
    ```
    ​A.*a[0]

    B.a[0]

    C.&a[0]

    D.p[0]

 

3. 以下程序的运行结果是
    ```cpp
    void sub(int x,int y,int *z){*z = y - x;}
    int main(){
    int a,b;
    sub(10,5,&a);
    sub(7,a,&b);
    cout<<a<<","<<b;
    } 
    ```

    A. -5,-12

    B.5,2

    C.-5,-2

    D.5,-2


4. 以下程序的报错位点是

    ```CPP
    int main(){
    int k=2,*ptr1=&k,*ptr2=&k;
    k=*ptr1+*ptr2;//A
    ptr2=k;//B
    ptr1=ptr2;//C
    k=*ptr1*(*ptr2);//D
    } 
    ```

5. 下面程序的运行结果是

    ```CPP
    char* s==”abcde”;s+=2;cout<<s;
    ```
    A. 编译报错

    B.cde

    C.c

    D.输出c字符的地址

 

6. 已有定义 ``char a[]=”xyz”,b[]={’x’,’y’,’z’}``，则下列说法正确的是：

    A. 数组a和b的长度相同

    B. 数组a的长度大于b的长度

    C. 数组a的长度小于b的长度

    D. 以上说法都不正确

 

7. 关于语句``int *ptr();``下列说法正确的是

    A. ptr是一个指针变量

    B. *ptr是一个函数名

    C. 这个语句是函数定义的语句

    D. ptr是一个函数名，函数返回值是指向int型数据的指针

 

8. 若有语句``int *point, a=4;``和``point=&a;``下面均代表地址的一组选项是

    A. a, point,*&a

    B.&*a, &a,*point

    C.*&point,*point,&a

    D.&a,&*point, point

 

二、阅读程序，写出运行结果

1. 阅读程序，写出运行结果

    ```CPP
    #include<iostream> 
    using namespace std;
    void f(int &x,int y){
        y = x + y;
        x = y % 3;
        cout<<x<<'\t'<<y<<endl;
        return ;
    } 

    int main(){
        int x=10,y=19;
        f(y,x);
        cout<<x<<'\t'<<y<<endl;
        f(x,x);
        cout<<x<<'\t'<<y<<endl;
        return 0;
    }
    ```



2. 设有一个矩阵$T=\left[\begin{array}{lll}0 & 2 & 1 \\1 & 0 & 2 \\1 & 2 & 0\end{array}\right]$，现在把它放在一个二维数组a中。写出执行下面的语句之后a的值.

    ```CPP
    #include<iostream> 
    using namespace std;
    int main(){
        int a[3][3]={{0,2,1},{1,0,2},{1,2,0}};
        for(int i=0;i<2;i++)
            for(int j=0;j<2;j++)
                a[i][j] = a[a[i][j]][a[j][i]];
        for(int i=0;i<=2;i++){
            for(int j=0;j<=2;j++)
                cout<<a[i][j]<<" ";
            cout<<endl;
        }
    } 
    ```

三、编程题

1. 完成函数体编写。要求返回一个一维数组中最大元素的地址。

    ```CPP
    int *max(const int x[],int num);
    ```

