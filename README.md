# BDM2020
Source codes for BDM2020 mohabike project

## フォルダ構成
- notinuse: 使わないもの
- static: webページ描画用。cssとか
- templates: webページ描画用。htmlファイル
- main.py: まずこれを立ち上げる
- pwm.c: main.pyから呼び出される、速度読取および波形出力を行うプログラム

## 使い方
1. pwm.cを以下のようにコンパイルする `gcc -o pwm_車両の名前.o -lm -lbcm2835 pwm.c`
2. main.pyを立ち上げる
3. ブラウザで `http://ラズパイのIP:50050` にアクセス
4. ブラウザの「車両を選択」で音を鳴らす車両を選ぶ。車両の名前は、main.pyと同一フォルダにある.o実行バイナリの_以降に対応している
5. 「主回路投入」を押すと実行バイナリが起動し、音を鳴らす準備ができる
