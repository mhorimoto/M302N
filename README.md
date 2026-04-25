# M302N3

New hardware that improves on the M302K to make it smaller, more dedicated and no-code.

M302Kを改良して小型化、専用化とノーコード化を目指した新しいハードウェア  
M302N2を使用して、
* 気温湿度
* CO2
* 光量子 or 日射量
* 土中水分

を1台で観測可能とする

ここまでが M302N2-ULTRA これからが、M302N3 本当のPoEを採用する

## Main specifications

## パーツリスト

N3のための新規パーツ（現在検討中）

+ RJ-45モジュール Pulse YAGEO J00-0065NL
+ PoE モジュール Silvertel Ag9912-MT 12V出力の工業規格

## 主諸元
+ I2CとADC入力を備えたUECS測定ノード機
+ I/Oは5V
+ 電源電圧はDC12V/1A(Max)
+ M800系のPoEは使えなくなる

## Revision List

### 1.00 初版 (2025/03/09)
### 2.00 
* J1の結線ミスを修正 (Done 2025/05/12)
* J2のUARTはSoftwareSerial対応にして、D0,D1を空けておき、D8,D9をRX,TXに割り当てる。5V Vccの追加。 (Done 2025/05/12)
* J3の対応ピンを変更する。Hardware InterruptのD2,D3を入力端子として扱えるように。D2,3,4,5,6,7 (Done 2025/05/12)
* LED-D2はA0に割り当てる
* J9,J10 の削除 (Done 2025/05/12)
* J11 止め穴を0.1mm大きくする
* SW1はXH-B2Bに変更 (Done 2025/05/12)
* J1へCPUから5Vが逆流しないように1S4を追加 (Done 2025/05/12)
### 3.00
