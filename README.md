# 2020cce
## 6/24程式
### week18-1
```java=
import processing.video.*;
Capture cam;
void setup()
{
  size(640,480);
  println( Capture.list() );
}
```
![](https://i.imgur.com/umJk2BP.jpg)
### week18-2
```java=
import processing.video.*;
Capture cam;
void setup()
{
  size(640,480);
  println( Capture.list() );
  cam=new Capture(this,"HD WebCam");
  cam.start();
}
void draw()
{
  if(cam.available()) cam.read();
  set(0,0,cam);
}
```
![](https://i.imgur.com/RxwK9Um.jpg)
### week18-3
```java=
import processing.video.*;
Movie movie;
void setup()
{
  size(640,480);
  movie=new Movie(this,"檔名.mov");
  movie.play();
}
void draw()
{
  if(movie.available())movie.read();
  set(0,0,movie);
}
```
![](https://i.imgur.com/6cnVvqJ.jpg)