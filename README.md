# LED_Device_Driver
2021年度ロボットシステム学の課題1で作成しその後改良したデバイスドライバです。

入力数字（0～6）に応じたledが消灯や点灯また、電子ブザーが鳴ったりします。

# 動作環境
Raspberry Pi3 Model B

OS: ubuntu 20.04 server

# 使用したもの
Raspberry Pi3 Model B

LED ×4

抵抗220Ω　×4

電子ブザー

ブレッドボード

ジャンパー線（オス‐メス）　×10

# 配線図



# 使用方法
# 「インストール」
$ git clone git@github.com:Masashi-Okada/robosys1.git

$ cd robosys1

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

# 「アンインストール」
$ sudo rmmod myled

$ make clean

# 「実行」
※　ページ下にデモ動画を参照
# 動作を止める
$ echo 0 > /dev/myled0
# ledを全てつける
$ echo 1 > /dev/myled0 
# ledとブザー全てつける
$ echo 2 > /dev/myled0 
# ledを同時につけたり消したりする
$ echo 3 > /dev/myled0 
# ブザーを鳴らす
$ echo 4 > /dev/myled0 
# ブザーを鳴らしたり消したりする
$ echo 5 > /dev/myled0 
# ledを順番につけたり消したりする
$ echo 6 > /dev/myled0 

# デモ動画

# ライセンス
GNU General Public Licence v3.0

Copyright (c) 2021 Ryuichi Ueda & Itsuki Ueno & Masashi Okada. All right reserved.
