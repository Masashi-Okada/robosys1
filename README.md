# LED_Device_Driver
2021年度ロボットシステム学の課題1で改良したデバイスドライバです。

0～6の入力数字に応じたledが消灯や点灯また、電子ブザーが鳴ったりします。

また、連続して点灯や消灯を繰り返し行います。


# 動作環境
Raspberry Pi3 Model B

OS: ubuntu 20.04 server

# 使用したもの
Raspberry Pi3 Model B

ブレッドボード

ジャンパー線（オス‐メス）　×10

LED ×4

電子ブザー

抵抗220Ω　×5


# 回路図
![image](https://user-images.githubusercontent.com/92083106/146315685-fa5f8062-741b-4a9b-9193-18b106f8e093.png)

# 配線図
![image](https://user-images.githubusercontent.com/92083106/146252105-9ab0c7ee-3a8c-41b0-9679-5fcace129244.png)



# 使用方法
# 「インストール」

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

# 「アンインストール」
$ sudo rmmod myled

$ make clean

# 「編集」
$ vi myled.c

$ vi Makefile

# 「実行」
https://youtu.be/GKRFipL725E
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

# ライセンス
GNU General Public License v3.0
詳細はCOPYINGを確認してください。

# 参照
上野樹さん（__delayの使用方法について）

# コントリビューション
ledの数やブザーを追加し点灯、消灯させる。

__delayを用いてledやブザーの点灯や消灯を繰り返す。

# 謝辞
今井悠月さんのreadmeを基にこちらを作成しました。
