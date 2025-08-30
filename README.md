# Gravity45 Vial Firmware

## About

[Greenkeys](https://green-keys.info/) が販売している [Gravity45](https://green-keys.info/lp/gravity45/) のVial対応ファームウェア公開用repositoryです。

## Download

[Releases](https://github.com/karbou12/gravity45_vial/releases) ページから、最新VersionのAssetsをクリックして表示される green_keys_gravity_45_vial.uf2 をダウンロードしてください。

## Install

[Greenkeysのビルドガイド](https://green-keys.info/lp/gravity45-build-guide/#vial) を参考に、ダウンロードしたファームウェアをインストールしてください。  
あるいは、RemapでBootloaderを任意のキーに割り当てて、Bootloaderキーを押してBootloaderモードにしてから、ファームウェアをインストールしてください。

>[!TIP]
>- RESET / REBOOTボタンを押すにはアクリルケースを外す必要があるので、bootloaderキーを割り当てるのをお勧めします。
>- Vial対応ファームウェアをインストール後は、Vialの[Security]→[Reboot to bootloader]メニューからBootloaderモードにすることもできます。

Remap版に戻したい場合は、[GreenkeyのFAQ](https://green-keys.info/gravity45-faq/#index_id29) を参照してください。

## Keymapの引き継ぎ方法

>[!IMPORTANT]
ファームウェアをインストールすると、KeymapがResetされるため、Keymapを引き継ぐにはインストール前に準備が必要です。

**A. Remapで設定したkeymapをVialでも引き継ぎたい場合**  
1. Remapでkeymapを保存してください。Google または Githubアカウントでのloginが必要です。
2. Vialファームウェアをインストールしてください。
3. Remapを開いてください。[Remap for QMK 0.18] を使うようメッセージが出るので、画面下の同メニューをクリックして、[START REMAP FOR YOUR KEYBOARD] メニューをクリックしてください。
5. 1で保存したkeymapを読み込んで[flash]ボタンを押してください。

**B. Vialファームウェアを再インストール または 更新版をインストールした後でもkeymapを引き継ぎたい場合**  
1. Vial画面上で[File]→[Save current layout]メニューをクリックしてファイル保存してください。
2. Vialファームウェアをinstallしてください。
3. Vial画面上で[File]→[Load saved layout]メニューをクリックして、1で保存したファイルを選択してください。

## Usage of Vial

[Vial](https://get.vial.today/)から、[Start Vial Web]をクリックしてWeb版を使用するか、[Download Vial]をクリックしてアプリ版を使用してください。  
Vialの一般的な使用方法については、[Vialのドキュメント](https://get.vial.today/manual/) やWebを検索してください。

## 本ファームウェア独自の設定について

### Layer毎のRGB-LED

Gravity45は中央キーのみRGB LEDが搭載されています。本Vial対応ファームウェアでは、Layerを切り替えたら、RGB LEDの色が変更するようになっています。Caps Wordが有効な時も色が変更されます。  
Vial上、または、キー入力によるRGB操作は、Default LayerのRGB LEDに適用されます。輝度だけは、各LayerのRGB LEDにも反映されます。

**Q.Layer切替時にLEDの色が変更されない、または、Layer切替時にLEDの色を変更したくない**  
A.Toggle Keyを用意していますので、[Keymap]->[User]から[RGB_LAYER_TOG (LYR_TOG)]を任意のキーに割り当てて、割り当てたキーを押して ON / OFF を切り替えてください。  
一度切り替えたら設定を保持していますので、不要でしたらキーの割り当てを外してください。

**Q.Default Layerに戻った時、あるいは、Caps Wordを抜けた時に、色が戻らない**  
A.一度キーボードのUSBケーブルを抜いて、再接続したら戻る場合があります。再接続でも元に戻らない場合は、色を再設定してください。

**Q.各Layerの色を自分で変更したい**  
A.Vialでは変更する手段はありません。ファームウェアをビルドする環境を自前で準備して、ソースコードをfolkして色を変更してください。

## Source Code

本Vial Firmware用のソースコードは[こちら](https://github.com/karbou12/vial-qmk/tree/keyboard/gravity45/keyboards/green_keys/gravity_45/keymaps/vial)になります。  
Gravity45設計者のtakashicompany さんの [VIA用コード](https://github.com/takashicompany/qmk_firmware/tree/master/keyboards/green_keys/gravity_45)を元に作成しています。

##

>[!CAUTION]
>- 本ファームウェアに関して、Greenkeysさんのサポートはありません。開発者が分かる範囲でサポートしますが、基本的には自己責任でご利用ください。
>- Mac環境で作成し、Mac環境でのみ動作確認をしています。Windows環境でも初版の動作確認はしましたが保証はできません。
>- 本ファームウェアを使用したことによるいかなる損害についても、開発者は一切の責任を負いません。
