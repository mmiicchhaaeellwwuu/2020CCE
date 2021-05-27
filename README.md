# 2020cce
## 5/27程式
### week14-1
```java=
void setup()
{
  float ans=random(60);
  text(ans,20,20);
}
void draw()
{
   
}
```
![](https://i.imgur.com/QR8zsFq.jpg)
### week14-2
```java=
int ans=0;
void setup()
{
  textSize(30);
}
void draw()
{
  background(#F2330C);
  text(ans,20,30);
}
void mousePressed()
{
  ans=(int)random(60);
}
```
![](https://i.imgur.com/9mWqiJT.jpg)
### week14-3
```java=
int []a={1,2,3,4,5,6,7,8,9,10};
int i1,i2;
void setup()
{
  size(400,100);
  textSize(30);
}
void draw()
{
  background(#F2330C);
  for(int i=0;i<10;i++)
  {
    text(a[i],i*40,50);
  }
  rect(i1*40,50,30,30);
  rect(i2*40,50,30,30);
}
void mousePressed()
{
  i1=(int)random(10);
  i2=(int)random(10);
  int temp=a[i1]; a[i1]=a[i2]; a[i2]=temp;
}
```
![](https://i.imgur.com/MngQ7Yw.jpg)
### week14-4
```java=
int []a=new int[47];
void setup()
{
  size(500,200);
  textSize(30);
  for(int i=0;i<47;i++) a[i]=i;
  
  for(int i=0;i<1000;i++)
  {
      int i1=(int)random(47);
      int i2=(int)random(47);
      int temp=a[i1]; a[i1]=a[i2]; a[i2]=temp;
  }
}
void draw()
{
    background(#6F1301);
    for(int i=0;i<5;i++)
    {
        text(a[i],i*80,100);
    }
}
```
![](https://i.imgur.com/N7cOyTa.jpg)
### week14-5
```java=
int []a=new int[47];
void setup()
{
  size(500,200);
  textSize(30);
  for(int i=0;i<47;i++) a[i]=i;
  
  for(int i=0;i<1000;i++)
  {
      int i1=(int)random(47);
      int i2=(int)random(47);
      int temp=a[i1]; a[i1]=a[i2]; a[i2]=temp;
  }
}
int N=0;
void draw()
{
    background(#6F1301);
    for(int i=0;i<N;i++)
    {
        text(a[i],i*80,100);
    }
}
void mousePressed()
{
  N++;
}
```
![](https://i.imgur.com/5CyLUCq.jpg)
### week14-6
```java=
int []a=new int[47];
void setup()
{
  size(500,200);
  textSize(30);
  for(int i=0;i<47;i++) a[i]=i;
  
  for(int i=0;i<1000;i++)
  {
      int i1=(int)random(47);
      int i2=(int)random(47);
      int temp=a[i1]; a[i1]=a[i2]; a[i2]=temp;
  }
}
int N=0;
void draw()
{
  background(#6F1301);
  textAlign(CENTER,CENTER);
  for(int i=0;i<N;i++)
  {
    fill(255); ellipse(i*80+40,100,55,55);
    fill(0);   text(a[i],i*80+40,100);
  }
}
void mousePressed()
{
  N++;
}
```
![](https://i.imgur.com/ntfuLWU.jpg)