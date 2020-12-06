# myled
ロボットシステム学　課題1

# １．課題内容  
講義内で作成したプログラムを参考に自身で改造したプログラムを作成せよ。

# ２．環境  
Raspberry Pi4(ubuntu20.04 LTS)  
LED2個、220Ω抵抗2個、ジャンパーワイヤ5本、ブレットボード1個

# ３．改造点  
LEDを2個使用。  
GPIOの24番,26番を使用。  
点灯、消灯の他に同時点滅、交互に点滅する動作を加えた。  
（0:消灯　1:点灯　2:同時点滅　3:交互点滅）

# ４．実行手順  
make  
sudo rmmod myled  
sudo insmod myled.c  
sudo chmod 666 /dev/myled0  
echo 1 > /dev/myled0   
echo 0 > /dev/myled0      
echo 2 > /dev/myled0   
echo 3 > /dev/myled0
