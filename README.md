# M302N

New hardware that improves on the M302K to make it smaller, more dedicated and no-code.

M302Kを改良して小型化、専用化とノーコード化を目指した新しいハードウェア

## Main specifications



## 主諸元
+ I2CとADC入力を備えたUECS測定ノード機
+ I/Oは5V
+ 電源電圧はDC12V/1A(Max)
+ M800系のPoEとACアダプタなどの外部電源のどちらも使える

## Revision List

### 1.00 初版 (2025/03/09)
### 2.00 
* J1の結線ミスを修正 (Done 2025/05/12)
* J2のUARTはSoftwareSerial対応にして、D0,D1を空けておく。5V Vccの追加。 (Done 2025/05/12)
* J3の対応ピンを変更する。Hardware InterruptのD2,D3を入力端子として扱えるように。D2,3,4,5,6,7 (Done 2025/05/12)
* LED-D2はDIO9に割り当てる
* J9,J10 の削除 (Done 2025/05/12)
* J11 止め穴を0.1mm大きくする
* SW1はXH-B2Bに変更 (Done 2025/05/12)
* J1へCPUから5Vが逆流しないように1S4を追加 (Done 2025/05/12)
* 