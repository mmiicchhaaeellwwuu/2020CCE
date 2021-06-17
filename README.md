# 2020cce
## 6/17程式
### week17-1
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
String line="hello";
void draw()
{
  background(#FAD412);
  text(line,100,100);
  text("World",100,150);
}
```
![](https://i.imgur.com/XQxhIk3.jpg)
### week17-2
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
String line="hello";
char c='9';
void draw()
{
  background(#FAD412);
  text(line+c,100,100);
  text("World:"+key,100,150);
}
```
![](https://i.imgur.com/2mKV8X1.jpg)
### week17-3
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
char c='9';
int win=0;
void draw()
{
  background(#FAD412);
  text("Press:"+c,100,100);
  text("You  "+key,100,150);
  if(c==key) win=1;
  else win=0;
  if(win==1) text("You win!",100,50);
}
```
![](https://i.imgur.com/nsYbLxK.jpg)
### week17-4
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
char c='9';
String ans="abcdefghijklmnopqrstuvwxyzACDEFGHIJKLMNOPQRSTUVWXYZ";
int win=0;
void draw()
{
  background(#FAD412);
  text("Press:"+c,100,100);
  text("You  "+key,100,150);
  if(c==key) win=1;
  else win=0;
  if(win==1)
  {
    text("You Win!",100,50);
    int i=int(random(26+26));
    c=ans.charAt(i);
  }
}
```
![](https://i.imgur.com/FlIeIzY.jpg)
### week17-5
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
int x=100,y=100;
void draw()
{
  background(#FAD412);
  rect(x,y,50,50);
}
void keyPressed()
{
  if(keyCode==LEFT) x-=10;
  if(keyCode==RIGHT) x+=10;
}
```
![](https://i.imgur.com/QPfqvoL.jpg)
### week17-6
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
float x=100,y=100,vx=0,vy=0;
void draw()
{
  background(#FAD412);
  rect(x,y,50,50);
  x+=vx;
}
void keyPressed()
{
  if(keyCode==LEFT) vx-=1;
  if(keyCode==RIGHT) vx+=1;
}
void keyReleased()
{
  vx=0;
}
```
![](https://i.imgur.com/y1OTuUQ.jpg)
### week17-7
```java=
String A="mother";
String line="";
void setup()
{
  size(400,300);
  textSize(40);
}
void draw()
{
  background(0);
  text(A,100,100);
  text(line+"|",100,150);
}
void keyPressed()
{
  line=line+key;
}
```
![](https://i.imgur.com/IAp83Jt.jpg)
### week17-8
```java=
String A="mother";
String line="";
void setup()
{
  size(400,300);
  textSize(40);
}
void draw()
{
  background(0);
  text(A,100,100);
  text(line+"|",100,150);
}
void keyPressed()
{
  int len=line.length();
  if(key>='a'&&key<='z') line=line+key;
  if(key>='A'&&key<='Z') line=line+key;
  if(key==ENTER){  }
  if(key==BACKSPACE&&len>0) line=line.substring(0,len-1);
}
```
![](https://i.imgur.com/P7fPRLr.jpg)
