# device_driver
ロボットシステム学で作成したデバイスドライバ

## 内容
https://github.com/ryuichiueda/robosys_device_drivers/blob/master/myled.c を改変して複数のLEDライトを光らせました作成しました。

## 使用したもの
・Raspberry Pi4 1個  
・10mm赤色LED　OS5RAAA131A 5個  
・ブレッドボード　EIC-801 1個  
・ブレッドボード・ジャンパーワイヤ（オス－メス）15cm 黒 10本  
・カーボン抵抗（炭素皮膜抵抗） 1/4W330Ω 5個
## 動かし方
myledとMakefileを作り  
make  
↓  
sudo insmod myled.ko  
↓  
sudo chmod 666 /dev/myled0  
↓  
echo 1 > /dev/myled0
## 動画
https://youtu.be/HPHcSGwn6U0
