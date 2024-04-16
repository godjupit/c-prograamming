# 函数
## 函数传参
```c
#include<stdio.h>
void swap(int *p,int *b)//在函数中，这里叫形参，这种情况下就可以调用指针
//这里不返回任何值，因此用void,int *p和int *b是两个参数
{
    int z = *p;
    *p = *b;
    *b = z;
}
int main(void)
{
    int a, b;
    scanf("%d%d",&a,&b);
    swap(&a,&b);//这里是实参，形参的改变不影响实参
    printf("%d %d",a,b);
    return 0;
}
```
## 函数返回值
没有返回值的函数要被定义为void function(),代表返回空值
有返回值的函数，返回值回到函数的地方，可以赋给变量
```c
#include <stdio.h>
int add(int a, int b) {
    return a + b;
}
int main() {
    int result = add(3, 5);//函数的返回值返回a+b 到result上
    printf("The result is: %d\n", result);
    return 0;
}

```
## 函数嵌套
函数可以嵌套调用，但是不能嵌套定义
## 链式访问
```c
#include<stdio.h>
#include<string.h>

int main(void)
{
    printf("%d",strlen("jingji")); //链式访问 函数的返回值作为其他函数的参数
    return 0;
}
```
## 函数模块化
可以创立头文件加源文件的集合来使函数功能模块化  
### 函数头文件：将.h文件中的内容拷贝到main函数中
### 声明和定义分开
实现模块化时，头文件里存放函数声明，同时用一个源文件存放函数主体

## 函数递归