# device_driver
ロボットシステム学で作成したデバイスドライバ

## 内容
上田隆一教授が授業で作成したデバイスドライバ(https://github.com/ryuichiueda/robosys_device_drivers/blob/master/myled.c )を改変して複数のLEDライトを光らせるものを作成しました。
## 動作環境 
OS:Ubuntu 18.04 
## 使用したもの
・Raspberry Pi4 1個  
・10mm赤色LED　OS5RAAA131A 5個  
・ブレッドボード　EIC-801 1個  
・ブレッドボード・ジャンパーワイヤ（オス－メス）15cm 黒 10本  
・カーボン抵抗（炭素皮膜抵抗） 1/4W330Ω 5個
# インストール方法  
``` 
$ git clone https://github.com/himiz815/device_driver.git  
```
## 動かし方

myledとMakefileを作り 
``` 
$ make  
```
↓  
``` 
$ sudo insmod myled.ko  
```
↓  
```
$ sudo chmod 666 /dev/myled0
```
↓  
``` shell
$ echo 1 > /dev/myled0
```
でLEDが光り始めます　
## 動画
https://youtu.be/HPHcSGwn6U0
## ライセンス
[GNU General Public License v3.0](https://github.com/kiyoshirou-kawanabe/Robosys_Devicedriver/blob/main/COPYING)
