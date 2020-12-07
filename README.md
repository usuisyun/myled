# myled
ロボットシステム学　課題1

# １．課題内容  
講義内で作成したプログラムを参考に自身で改造したプログラムを作成せよ。

# ２．環境  
Raspberry Pi4(ubuntu20.04 LTS)  
LED2個、220Ω抵抗2個、ジャンパーワイヤ5本、ブレットボード1個

# ３．実装内容 
LED2個を間に抵抗を挟んでGPIOの24番,26番に接続。　　  <img width="524" alt="2020-12-07" src="https://user-images.githubusercontent.com/75220169/101298444-539a1980-3871-11eb-87ca-cf763e62af0a.png">
講義で行った点灯、消灯の他に同時点滅、交互に点滅する動作を加えた。  
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

　
