# myled
ロボットシステム学　課題1

# １．概要  
講義内で作成したプログラムを参考に自身で改造し、LEDを2個に増やして同時点滅、交互に点滅を行うプログラム。

# ２．環境  
Raspberry Pi4(ubuntu20.04 LTS)  
LED2個、220Ω抵抗2個、ジャンパーワイヤ5本、ブレットボード1個

# ３．実装内容 
下図のように各LEDのアノードをGPIOの24番,26番に接続。各LEDのカソードとGNDを抵抗を間に入れて接続。  <img width="524" alt="2020-12-07" src="https://user-images.githubusercontent.com/75220169/101298444-539a1980-3871-11eb-87ca-cf763e62af0a.png">  
講義で行った点灯、消灯の他に同時点滅、交互に点滅を行うようにした。それぞれ0,1,2,3を入力することで動作する。  
（0:消灯　1:点灯　2:同時点滅　3:交互点滅）

# ４．インストール・実行手順  
`git clone https://github.com/usuisyun/myled.git`  
`cd myled`  
`make`      
`sudo insmod myled.ko`  
`sudo chmod 666 /dev/myled0`  

`echo 1 > /dev/myled0` 点灯  
`echo 0 > /dev/myled0` 消灯  
`echo 2 > /dev/myled0` 同時点滅  
`echo 3 > /dev/myled0` 交互点滅  　　　　　

# ５．デモ動画
https://youtu.be/Pso4gnbq0T8

# ６．ライセンス　　
GNU General Public License v3.0
　
