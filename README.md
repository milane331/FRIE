# FRIE
setup // 只做一次
loop // 迴圈 做無限次
pinMode(3,OUTPUT);// 宣告數位腳=3腳 輸出
digitalWrite(3,LOW);// LED暗掉
delay(500);//延遲 為了能用肉眼看到按跟亮
digitalWrite(3,HIGH);// LED亮起來
delay(500);//延遲 為了能用肉眼看到按跟亮
![image](https://github.com/milane331/FRIE/blob/master/6CEC108F-4D60-4258-8907-188484560277.jpeg)
在左邊有一個3v3那端是3伏特另一端如果=0則二極體導通LED恆亮
如果=1則無導通 LED不亮
