# 2020cce
## 10-1
```c=
#include <stdio.h>
char line[10000];
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for(int i=0;i<n;i++)
	{
		gets(line);
		
		printf("%s\n",line);
	}
}
```
![](https://i.imgur.com/LBFwI7i.png)
## 10-2
```c=
#include <stdio.h>
char line[10000];
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for(int i=0;i<n;i++)
	{
		gets(line);
		
		for(int k=0;line[k]!=0;k++)
		{
			char c=line[k];
			if(c>='A'&&c<='Z') printf("大");
			else if(c>='a'&&c<='z') printf("小");
			else printf("他");
		}
		
	}
}
```
![](https://i.imgur.com/YQ8oCSG.png)
## 10-3
```c=
#include <stdio.h>
char line[10000];
int ans[26];
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for(int i=0;i<n;i++)
	{
		gets(line);
		
		for(int k=0;line[k]!=0;k++)
		{
			char c=line[k];
			if(c>='A'&&c<='Z') ans[c-'A']++;
			else if(c>='a'&&c<='z') ans[c-'a']++;
		}
	}
	for(int i=0;i<26;i++)
	{
		printf("%c %d\n",'A'+i,ans[i]);
	}
}
```
![](https://i.imgur.com/UDWgpgk.png)
## 10-4
```c=
#include <stdio.h>
char line[10000];
int ans[26];
char alphabet[]="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for(int i=0;i<n;i++)
	{
		gets(line);
		
		for(int k=0;line[k]!=0;k++)
		{
			char c=line[k];
			if(c>='A'&&c<='Z') ans[c-'A']++;
			else if(c>='a'&&c<='z') ans[c-'a']++;
		}
	}
	for(int i=0;i<26;i++)
	{
		for(int j=i+1;j<26;j++)
		{
			if(ans[i]<ans[j]||(ans[i]==ans[j]&&alphabet[i]>alphabet[j]))
			{
				int temp=ans[i];
				ans[i]=ans[j];
				ans[j]=temp;
				char c=alphabet[i];
				alphabet[i]=alphabet[j];
				alphabet[j]=c;
			}
		}
	}
	for(int i=0;i<26;i++)
	{
		if(ans[i]>0) printf("%c %d\n",alphabet[i],ans[i]);
	}
}
```
![](https://i.imgur.com/6HeJMOX.png)
## 10-5
```c=
#include <stdio.h>
#include <stdlib.h>
char line[10000];
typedef struct
{
	int ans;
	char c;
}BOX;
BOX array[26];
int compare(const void *p1,const void *p2)
{
	if(((BOX*)p1)->ans >((BOX*)p2)->ans) return -1;
	else if(((BOX*)p1)->ans <((BOX*)p2)->ans) return +1;
	else if(((BOX*)p1)->c <((BOX*)p2)->c) return -1;
	else if(((BOX*)p1)->c >((BOX*)p2)->c) return +1;
	else return 0;
}
int main()
{
	for(int i=0;i<26;i++)
	{
		array[i].c='A'+i;
	}
	int n;
	scanf("%d\n",&n);
	for(int i=0;i<n;i++)
	{
		gets(line);
		for(int k=0;line[k]!=0;k++)
		{
			char c=line[k];
			if(c>='A'&&c<='Z') array[c-'A'].ans++;
			else if(c>='a'&&c<='z') array[c-'a'].ans++;
		}
	}
	qsort(array,26,sizeof(BOX),compare);
	for(int i=0;i<26;i++)
	{
		if(array[i].ans>0) printf("%c %d\n",array[i].c,array[i].ans);
	}
}
```
![](https://i.imgur.com/weK1Mxd.png)
