# 2020cce
# 正課程式
## 程式一
```c=
#include<stdio.h>
int a[5]={0,10,20,30,40};
int main()
{
    int *p=&a[2];
    *p=222;
    
    p+-2;
    *p=666;
}
```
![](https://i.imgur.com/xoVwxKR.png)
## 程式二
```c=
#include<stdio.h>
int a[5]={0,10,20,30,40};
int main()
{
    int *p=&a[2];
    *p=222;
    
    p+-2;
    *p=666;
    
    p--;
    *p=555;
}
```
![](https://i.imgur.com/Om3rB5a.png)
## 程式三
```c=
#include<stdio.h>
int a[5]={0,10,20,30,40};
int main()
{
    int *p=&a[2];
    *p=222;
    
    p+-2;
    *p=666;
    
    int *p2=p+4;
    *p=666;
    
    p--;
    *p=555;
}
```
![](https://i.imgur.com/ba2Rwgb.png)
## 程式四
```c=
#include<stdio.h>
#include<stdlib.h>

int a[10];
int main()
{
    int b[10];
    
    int *p= (int*)malloc(sizeof(int)*10);
}
```
![](https://i.imgur.com/8F6QrzY.png)
