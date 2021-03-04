# 2020cce
# 第一次實習課程式
## 1.進階題：分式化簡
```c
#include <stdio.h>
int main()
{
	int a,b,c,A,B;
	scanf("%d%d",&a,&b);
	A=a;
	B=b;
	c=a%b;
	while(c!=0)
	{
		a=b;
		b=c;
		c=a%b;
	}
	printf("%d %d\n",A/b,B/b);
}
```
## 2.進階題：讀入整數反序列印
```C
#include <stdio.h>
int main()
{
	int a[10],b=0;
	for(int i=0;i<10;i++)
	{
		scanf("%d",&a[i]);
		if(a[i]==0) break;
		else b++;
	}
	for(int i=b-1;i>=0;i--)
	{
		printf("%d ",a[i]);
	}
	printf("\n");
}
```
## 3.進階題：A的B次方函數
```C
#include <stdio.h>
int MYPOWER(int a,int b)
{
	int ans=1;
	for(int i=1;i<=b;i++)
	{
		ans*=a;
	}
	return ans;
}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```
## 4.進階題：漸增數列相加
```C
#include <stdio.h>
int main()
{
	int a,ans=0;
	scanf("%d",&a);
	for(int i=1;i<=a-1;i++)
	{
		ans+=i*(i+1);
	}
	printf("%d\n",ans);
}
```
## 5.基礎題：找零錢
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	printf("%d=50*%d+5*%d+1*%d\n",a,a/50,a%50/5,a%50%5);
}
```
## 6.基礎題：因數個數
```C
#include <stdio.h>
int main()
{
	int a,b=0;
	scanf("%d",&a);
	for(int i=1;i<=a;i++)
	{
		if(a%i==0)
		{
			b++;
		}
	}
	printf("%d\n",b);
}
```
## 7.基礎題：找倍數
```C
#include <stdio.h>
int main()
{
	int a[10],b=0;
	for(int i=0;i<10;i++)
	{
		scanf("%d",&a[i]);
		if(a[i]%3==0)
		{
			b++;
		}
	}
	printf("%d\n",b);
}
```
## 8.基礎題：整數轉換為等級
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	if(a>=90) printf("A\n");
	else if(a>=80) printf("B\n");
	else if(a>=60) printf("C\n");
	else if(a< 60) printf("F\n");
}
```