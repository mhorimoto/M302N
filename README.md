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

### 3.00
* W5500をオンボード実装する。
* PoE(PD)デバイスを実装する準備。

## PoEを検討する

[技術情報](https://www.monolithicpower.com/jp/learning/resources/how-to-optimize-a-power-over-ethernet-pd-design?srsltid=AfmBOoqbZEuF42aN06ACb63LRKW16xLEzh97txKA_eJsGOTwgDsu3x3L)
[参考資料](https://www.kicad-de-kiban.net/archives/MKR_PoE_eth_shield1.html)

目指すは、802.3af class1 (4W)  
いくつかのデバイス候補を掲げる。

### Analog Devices
* LT4321 (Diode Bridge Controller)
* LT4295 (PD Controller)
* LTC4257: IEEE 802.3af PDインターフェースコントローラ。
* LT3798: 絶縁型フライバックコントローラ（DC-DCコンバータ用）。

### Texas Instruments:
* TPS23753A: 低消費電力、小型パッケージのPDコントローラ。
* TPS23754: 統合MOSFET、高効率のPDコントローラ。
* TPS23756: 同期整流コントローラ内蔵のPDコントローラ。
* TPS2378: 高集積、低スタンバイ電力のPDコントローラ。
* UCC2897A: 高効率フライバックコントローラ（DC-DCコンバータ用）。

### Monolithic Power Systems (MPS):
* MP8001/MP8001A: 15WまでのPoE PDコントローラ。
* MP8007/MP8007H: 13Wまでのフライバック/降圧コンバータ内蔵PDコントローラ。
### ON Semiconductor:
* NCP1095/NCP1096: 低電力PDコントローラ。

### M5Stackなどの参考回路から
* HBJ-6308ANLF  RJ45 for PoE これだけでDC出力が得られる？詳細調査中。
* WC-PD06H050A  PDコントローラーモジュール
  