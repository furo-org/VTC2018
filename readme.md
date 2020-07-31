﻿# VTC: Virtual Tsukuba Challenge

つくばチャレンジ 3rd stage の確認走行区間を模擬した環境と、そこで動作する移動ロボットシミュレータ。
[![VTC with lidar intensity enabled](docs/ScreenShot-i.png)](https://www.youtube.com/watch?v=gb9t7RFmgpc)

## 関連Repository

+ [Cage Plugin](https://github.com/furo-org/CagePlugin): 移動ロボット、センサ等の機能をパッケージしたプラグイン
+ [ZMQUE Plugin](https://github.com/furo-org/ZMQUE): ZeroMQのdllをロードするプラグイン
+ [PxArticulationLink Plugin](https://github.com/yosagi/PxArticulationLink): PhysX Articulation APIにアクセスするためのプラグイン
+ [CageClientライブラリ](https://github.com/furo-org/CageClient): シミュレータ内ロボットと通信し、コマンドを送りステータスを取得するライブラリ
+ [cage_ros_stack](https://github.com/furo-org/cage_ros_stack): CageClientライブラリのROSブリッジ

## 動作環境

以下の環境で動作確認しています。

PC

+ Ryzen7 1800X(3.6GHz) + GeForce GTX 1080
+ Core i7 7700HQ(2.8GHz) + GeForce GTX 1060

ソフトウェア環境

+ Windows 10 1909 64bit
+ Visual Studio 2019 16.5.4
+ Unreal Engine 4.25.2

## ドキュメント

+ [シミュレータの操作方法](docs/runtime.md)
+ [エディタでの開発環境設定](docs/editor.md)

環境を編集したり、シミュレータのコードに手を入れるにはエディタでの開発環境をセットアップする必要があります。既存の環境でロボットを走らせるだけならば、パッケージ済みバイナリと[CageClientライブラリ](https://github.com/furo-org/CageClient)または[cage_ros_stack](https://github.com/furo-org/cage_ros_stack)があれば十分です。

## パッケージ済みバイナリのダウンロード

+ [VTC 2020/5/28版 Windows 64bit 約1GB](https://1drv.ms/u/s!AkekAlL4McuXlQOBSBVlSNaRIZpQ?e=veg3e0)
+ [VTC2019 Windows 64bit 約750MB](https://chibakoudai-my.sharepoint.com/:u:/g/personal/yoshida_tomoaki_p_chibakoudai_jp/ETDQWwohngxKsu09_ga2H9UBs5A4OmVFnmzQckcgW8upzA?e=IJuMfI)
+ [VTC2018 (以前のバージョン) Windows 64bit 約700MB](https://chibakoudai-my.sharepoint.com/:u:/g/personal/yoshida_tomoaki_p_chibakoudai_jp/ER00YHh9YYFEpBnFCl16Ug4BnmRve_PuS1y1sB2-dvryDw?e=cxDaMb)

zipを展開してVTC.exe(もしくは古いものはVTC2018.exe)を起動するだけなので、各種アカウントの用意やインストールなどをせずに手軽に試せます。全画面とウィンドウモードの切り替えはAlt-Enterで、終了はAlt-F4もしくはEscです。パッケージ版はUnreal Editorで編集することはできませんが、[CageClientライブラリ](https://github.com/furo-org/CageClient)または[cage_ros_stack](https://github.com/furo-org/cage_ros_stack)を使ってコマンドを送ることでロボットを動かすことができますし、lidarのシミュレーションも動きます。

## License

VTCはApache2.0とします。

Copyright [2017-2020] Tomoaki Yoshida <yoshida@furo.org>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
