# Gravity45 Vial Firmware

<p align="center"><img src="/images/top_gravity45.jpeg" width="90%" /></p>

## About

[Greenkeys](https://green-keys.info/) が販売している [Gravity45](https://green-keys.info/lp/gravity45/) のVial対応ファームウェア公開用repositoryです。

<p align="center"><img src="/images/top_vial.png" /></p>

以下、簡易マニュアルとなります。キャプチャ付きの詳細マニュアルは[Wiki](../../wiki)を参照してください。

## Download

[Releases](https://github.com/karbou12/gravity45_vial/releases) ページから、最新VersionのAssetsをクリックして表示される green_keys_gravity_45_vial.uf2 をダウンロードしてください。

## Install

>[!IMPORTANT]
> ファームウェアをインストールすると、KeymapがResetされるため、Keymapを引き継ぐにはインストール前に準備が必要です。  
> [Keymapの引き継ぎ方法](#keymapの引き継ぎ方法)を事前に確認してください。

[Greenkeysのビルドガイド](https://green-keys.info/lp/gravity45-build-guide/#vial) を参考に、ダウンロードしたファームウェアをインストールしてください。

あるいは、RemapでBootloaderを任意のキーに割り当てて、Bootloaderキーを押してBootloaderモードにしてから、ファームウェアをインストールしてください。

> [!TIP]
> - RESET / REBOOTボタンを押すにはケースを外す必要があるので、Bootloaderキーを割り当てるのをお勧めします。
> その場合、Bootloaderキーは常設せず、ファームウェアをインストールする時だけ設定するのをお勧めします。
> - Vial対応ファームウェアをインストール後は、Vialの[Security]→[Reboot to bootloader]メニューからBootloaderモードにすることもできます。
> - VialでBootloaderを設定しようとすると、Unlock Modeにするために2個のキーの長押しを指示する画面が出ますので、指示に従い2キーを長押ししてください。

Remap版に戻したい場合は、[GreenkeysのFAQ](https://green-keys.info/gravity45-faq/#index_id29) を参照してください。

## Keymapの引き継ぎ方法

**A. Remapで設定したkeymapをVialでも引き継ぎたい場合**  

1. Remapでkeymapを保存してください。Google または Githubアカウントでのloginが必要です。  
2. Vialファームウェアをインストールしてください。
3. Remapを開いてください。[Remap for QMK 0.18] を使うようメッセージが出るので、画面下の同リンクをクリックして、[START REMAP FOR YOUR KEYBOARD] をクリックしてください。
4. 1で保存したkeymapを読み込んで、[flash]をクリックしてください。

**B. Vialファームウェアを再インストール または 更新版をインストールした後でもkeymapを引き継ぎたい場合**  

1. Vial画面上で[File]→[Save current layout]メニューをクリックしてファイル保存してください。
2. Vialファームウェアをinstallしてください。
3. Vial画面上で[File]→[Load saved layout]メニューをクリックして、1で保存したファイルを選択してください。

## Vial の使い方

[Vial](https://get.vial.today/)から、[Start Vial Web]をクリックしてWeb版を使用するか、[Download Vial]をクリックしてアプリ版を使用してください。  
Vialの一般的な使用方法については、[Vialのドキュメント](https://get.vial.today/manual/) やWebを検索してください。

## 本ファームウェア独自の設定について

- Layer毎のRGB-LED
  - Gravity45は中央キーのみRGB LEDが搭載されています。本Vial対応ファームウェアでは、Layerを切り替えたら、RGB LEDの色が変わるようになっており、ユーザーが各Layerの色を設定することができます。また、Caps Wordが有効な時も色が変わります。  
- OS毎のDefault Layer設定
  - OS毎にDefault Layerを設定できるようにしています。     

設定の詳細は[Wiki](../../wiki/User-Custom-Seetings)を参照してください。

## Troubleshooting

[Wiki](../../wiki/Troubleshooting)を参照してください。

## Source Code

[本Vial Firmware用のソースコード](https://github.com/karbou12/vial-qmk/tree/keyboard/gravity45/keyboards/green_keys/gravity_45/keymaps/vial)は、
Gravity45設計者のtakashicompany さんの [VIA用コード](https://github.com/takashicompany/qmk_firmware/tree/master/keyboards/green_keys/gravity_45)を元に作成しています。  
詳細は[Wiki](../../wiki/Source-Code)を参照してください。

##

>[!CAUTION]
>- 本ファームウェアに関して、Greenkeysさんのサポートはありません。開発者が分かる範囲でサポートしますが、基本的には自己責任でご利用ください。
>- Mac環境で作成し、Mac環境でのみ動作確認をしています。Windows環境でも初版の動作確認はしましたが保証はできません。
>- 本ファームウェアを使用したことによるいかなる損害についても、開発者は一切の責任を負いません。
