#2020cce
## 5/20程式
### week13-1
```java=
void draw()
{
  if(mousePressed) background(191,23,8);
  else background(27,8,255);
  text(a,512,200);
}
```
![](https://i.imgur.com/7trpcPs.jpg)
### week13-2
```java=
void draw()
{
  if(mousePressed) background(191,23,8);//暗紅色
  else background(27,8,255);//藍色
  text(a,512,200);
}
```
![](https://i.imgur.com/v9JxKYl.jpg)
### week13-3
```java=
void draw()
{
  if(mousePressed) background(191,23,8);//暗紅色
  else background(27,8,255);//藍色
  text(a,512,200);
}
int a=0;
void mousePressed()
{
  a++;
}
```
![](https://i.imgur.com/FXsmUwU.jpg)
### week13-4
```java=
void setup()
{
  size(1024,400);
}
void draw()
{
  if(mousePressed) background(191,23,8);//暗紅色
  else background(27,8,255);//藍色
  textSize(36);
  text("中文壞掉Now a is:"+a,212,200);
}
int a=0;
void mousePressed()
{
  a++;
}
```
![](https://i.imgur.com/LAL00Ls.jpg)
### week13-5
```java=
void setup()
{
  size(1024,400);
}
void draw()
{
  background(#FFF708);
  int s=second();
  int m=minute();
  int h=hour();
  textSize(80);
  text(h+":"+m+":"+s,100,200);
}
```
![](https://i.imgur.com/J6w4DyY.jpg)
### week13-6
```java=
void setup()
{
  size(1024,400);
  textFont(createFont("標楷體",80));
}
void draw()
{
  background(#FFF708);
  int s=second();
  int m=minute();
  int h=hour();
  textSize(80);
  text(h+":"+m+":"+s,100,200);
  int total=s+60*m+60*60*h;
  int closeH=17,closeM=40,closeS=0;
  int total2=closeS+60*closeM+60*60*closeH;
  int ans=total2-total;
  text("剩下幾秒:"+ans,100,100);
}
```
![](https://i.imgur.com/JdXKdP8.jpg)
### week13-7
```java=
void setup()
{
  size(1024,400);
  textFont(createFont("標楷體",80));
}
void draw()
{
  background(#FFF708);
  int s=second();
  int m=minute();
  int h=hour();
  textSize(80);
  text(h+":"+m+":"+s,100,200);
  int total=s+60*m+60*60*h;
  int closeH=17,closeM=40,closeS=0;
  int total2=closeS+60*closeM+60*60*closeH;
  int ans=total2-total;
  text("剩下幾秒:"+ans,100,100);
  int ansH=ans/60/60%60,ansM=ans/60%60,ansS=ans%60;
  text(ansH+":"+ansM+":"+ansS,100,300);
}
```
![](https://i.imgur.com/4vN8euh.jpg)
