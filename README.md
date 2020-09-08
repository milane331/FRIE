# FRIE

setup // 只做一次</br>
loop // 迴圈 做無限次</br>
pinMode(3,OUTPUT);// 宣告數位腳=3腳 輸出</br>
```c++
digitalWrite(3,LOW);// LED暗掉
```
delay(500);//延遲 為了能用肉眼看到按跟亮</br>
digitalWrite(3,HIGH);// LED亮起來</br>
delay(500);//延遲 為了能用肉眼看到按跟亮</br>
![image](https://github.com/milane331/FRIE/blob/master/6CEC108F-4D60-4258-8907-188484560277.jpeg)
在左邊有一個3v3那端是3伏特另一端如果=0則二極體導通LED恆亮</br>
如果=1則無導通 LED不亮</br>
```
new
int jj=0,pwm=1,j=0;//給變數一個初值
void setup() {
for(int i=2;i<6;i++)pinMode(i,OUTPUT);//以for 迴圈取2345腳為輸出
for(int i=2;i<6;i++)digitalWrite(i,0);//給LED 一個初值為0以免一開始就亮了
}

void loop() {
for(int i=2;i<6;i++)digitalWrite(i,jj);//2345以jj判定是否要亮
delay(200);//延遲 200 毫秒
jj^=1;//jj做互斥或 ex jj=1 和 1 互斥或 =0 所以不亮

呼吸燈   analogWrite類比輸出
/*for(int i=2;i<6;i++)analogWrite(i,j);
j+=pwm;
if(j>255)pwm=-1;//執行減滅
if(j<0)pwm=1;//執行增亮
delay(5);*/
}
跑馬燈
void loop() {
for(int i=5;i>1;i--){
digitalWrite(i,jj);
delay(20);
}
jj^=1;
