# 2020cce
## 6/10程式
### week16-1
```java=
void setup()
{
  size(400,200);
}
void draw()
{
  background(#0C33C9);
  ellipse(50,50,80,80);
}
```
![](https://i.imgur.com/G88h6Mb.jpg)
### week16-2
```java=
void setup()
{
  size(400,200);
}
void draw()
{
  background(#7D2A90);
  fill(255);
  ellipse(50,50, 80,80);
  fill(255,0,0);
  float stop=mouseX/50.0;
  text(stop,100,100);
  arc(50,50, 80,80, 0,stop);
}
```
![](https://i.imgur.com/CiKKDNp.jpg)
### week16-3
```java=
void setup()
{
  size(400,200);
}
void draw()
{
  background(#7D2A90);
  fill(255);
  ellipse(50,50, 80,80);
  fill(255,0,0);
  float start=mouseX/50.0;
  textSize(40);
  text(start,100,100);
  arc(50,50, 80,80, 0+start,0.1+start);
}
```
![](https://i.imgur.com/82ANxbh.jpg)
### week16-4
```java=
void setup()
{
  size(400,200);
}
void draw()
{
  background(#7D2A90);
  fill(255);
  ellipse(100,100, 180,180);
  fill(255,0,0);
  float start=mouseX/50.0;
  for(int i=0;i<24;i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(0);
    if(i%3==1) fill(#0FF08C);
    if(i%3==2) fill(255);
    arc(100,100, 180,180,shift+0+start,shift+PI/12+start);
  }
}
```
![](https://i.imgur.com/0kAappU.jpg)
### week16-5
```java=
void setup()
{
  size(400,200);
}
void draw()
{
  background(#7D2A90);
  fill(255);
  ellipse(100,100, 180,180);
  fill(255,0,0);
  float start=mouseX/50.0;
  for(int i=0;i<24;i++)
  {
    float shift=2*PI*i/24.0;
    if(i%3==0) fill(0);
    if(i%3==1) fill(#0FF08C);
    if(i%3==2) fill(255);
    if(i==0) fill(#0F1BF0);
    arc(100,100, 180,180,shift+0+start,shift+PI/12+start);
  }
}
```
![](https://i.imgur.com/BUxWC2f.jpg)
### week16-6
```java=
void setup()
{
  size(400,200);
}
float start=0;
void draw()
{
  background(#7D2A90);
  if(start<10) start+=0.01;
  fill(255); text(start,200,150);
  for(int i=0;i<24;i++)
  {
    float shift=i*PI/12;
    if(i%3==0) fill(#000000);
    if(i%3==1) fill(#0FF08C);
    if(i%3==2) fill(#FFFFFF);
    if(i==0) fill(#0F1BF0);
    arc(100,100, 180,180,shift+0+start,shift+PI/12+start);
  }
}
```
![](https://i.imgur.com/47SG8tX.jpg)
### week16-7
```java=
void setup()
{
  size(400,200);
}
float start=0,v=0.07;
void draw()
{
  background(#7D2A90);
  if(v>0.001)
  {
    start+=v;
    v*=0.99;
  }
  fill(255); text(start,200,150); text(v,200,170);
  for(int i=0;i<24;i++)
  {
    float shift=i*PI/12;
    if(i%3==0) fill(#000000);
    if(i%3==1)  fill(#0FF08C);
    if(i%3==2) fill(#FFFFFF);
    if(i==0) fill(#0F1BF0);
    arc(100,100, 180,180,shift+0+start,shift+PI/12+start);
  }
}
```
![](https://i.imgur.com/AszB4Md.jpg)
### week16-8
```java=
void setup()
{
  size(400,200);
}
float start=0,v;
void draw()
{
  background(#7D2A90);
  if(v>0.001)
  {
    start+=v;
    v*=0.99;
  }
  fill(255); text(start,200,150); text(v,200,170);
  for(int i=0;i<24;i++)
  {
    float shift=i*PI/12;
    if(i%3==0) fill(#000000);
    if(i%3==1)  fill(#0FF08C);
    if(i%3==2) fill(#FFFFFF);
    if(i==0) fill(#0F1BF0);
    arc(100,100, 180,180,shift+0+start,shift+PI/12+start);
  }
}
void mousePressed()
{
  v=random(1);
}
```
![](https://i.imgur.com/FL2xyNJ.jpg)