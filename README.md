# 2020cce
## 6/3程式
### week15-1
```java=
void setup()
{
  size(400,200);
}
void draw()
{
  int s=second();
  if(s%2==0) background(255,0,0);
  else background(58,114,191);
}
```
![](https://i.imgur.com/JCgz0EX.jpg)
### week15-2
```java=
void setup()
{
  size(400,200);
  textSize(40);
}
void draw()
{
  int s=second();
  background(58,114,191);
  text(10-s%11,100,100);
}
```
![](https://i.imgur.com/UV4yfU1.jpg)
### week15-3
```java=
import processing.sound.*;
SoundFile player;
void setup()
{
  size(400,200);
  player=new SoundFile(this,"tada.mp3");
}
void draw()
{
  background(51,114,191);
}
void mousePressed()
{
  player.play();
}
```
![](https://i.imgur.com/LN0wFwu.jpg)
### week15-4
```java=
import processing.sound.*;
SoundFile player;
void setup()
{
  size(400,200);
  player=new SoundFile(this,"bell.mp3");
}
void draw()
{
  background(51,114,191);
}
void mousePressed()
{
  if(player.isPlaying())
  {
    player.stop();
  }
  else
  {
    player.play();
  }
}
```
![](https://i.imgur.com/8YApzhw.jpg)
### week15-5
```java=
import processing.sound.*;
SoundFile player;
void setup()
{
  size(400,200);
  textSize(40);
  player=new SoundFile(this,"tada.mp3");
}
void draw()
{
  int s=second();
  background(58,114,191);
  text(10-s%11,100,100);
  if(10-s%11==0&&!player.isPlaying())
  {
    player.play();
  }
}
```
![](https://i.imgur.com/6UN5pZx.jpg)
### week15-6
```java=
function setup() {
  createCanvas(400,200);
}
function draw() {
  let s=second();
  if(s%2==0) 
  {
    background(255,0,0);
  }
  else 
  {
    background(58,114,191);
  }
}
```
![](https://i.imgur.com/xA69ggJ.jpg)
