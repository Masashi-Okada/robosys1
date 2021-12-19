# robosys1_LED
# 概要
ロボットシステム学の課題1を基に改良したデバイスドライバです。

0～3の入力に応じてledが消灯や点灯をします。

また、連続して点灯や消灯を繰り返し行います。


# 環境
Raspberry Pi3 Model B

OS: ubuntu 18.04 server

# 使用したもの
Raspberry Pi3 Model B

ブレッドボード

ジャンパー線（オス‐メス）　×8

LED （黄、青、赤、緑）

抵抗220Ω　×4


# 回路図
![image](https://user-images.githubusercontent.com/92083106/146666265-0cfb7829-b283-4fbc-a467-378b64bac22b.png)

# 配線図と各ledの配置
![image](https://user-images.githubusercontent.com/92083106/146666337-f059a100-1297-4139-ac56-73ca4cd1da0a.png)
![image](https://user-images.githubusercontent.com/92083106/146667225-51256322-77fc-4f95-b8c1-fd46453c1e45.png)





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

# 実行した様子
https://youtu.be/WJAezhWA7AA
# 動作説明
$ echo 0 > /dev/myled0

→　動作を止めます。

$ echo 1 > /dev/myled0 

→　ledを全てつけます。

$ echo 2 > /dev/myled0 

→　ledを同時につけたり消したりします。

$ echo 3 > /dev/myled0 

→　ledを順番につけたり消したりします。
# ライセンス
GNU General Public License v3.0

詳細はCOPYINGを確認してください。

# コントリビューション
ledの数を追加し点灯、消灯させます。

__delayの使用方法を基にmdelayを用いてledの点灯や消灯を同時に行ったり、順番に繰り返します。

# 参照と謝辞
itsukiuenoさんに__delayの使用方法を参考にしました。　https://github.com/itsukiueno/kadai1

yuzukiimaiさんのREADMEを基にこちらを作成しました。 https://github.com/yuzukiimai/robosys1

ありがとうございました。





