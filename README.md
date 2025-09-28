# Gravity45 Vial Firmware

<p align="center"><img src="/images/top_gravity45.jpeg" width="90%" /></p>

## About

[Greenkeys](https://green-keys.info/) が販売している [Gravity45](https://green-keys.info/lp/gravity45/) のVial対応ファームウェア公開用repositoryです。

<p align="center"><img src="/images/top_vial.png" /></p>

## Download

[Releases](https://github.com/karbou12/gravity45_vial/releases) ページから、最新VersionのAssetsをクリックして表示される green_keys_gravity_45_vial.uf2 をダウンロードしてください。

<p align="center"><img src="/images/dl_releases.png" /></p>

## Install

[Greenkeysのビルドガイド](https://green-keys.info/lp/gravity45-build-guide/#vial) を参考に、ダウンロードしたファームウェアをインストールしてください。

あるいは、RemapでBootloaderを任意のキーに割り当てて、Bootloaderキーを押してBootloaderモードにしてから、ファームウェアをインストールしてください。
<p align="center"><img src="/images/inst_remap_bootloader.png" /></p>

> [!TIP]
> RESET / REBOOTボタンを押すにはケースを外す必要があるので、Bootloaderキーを割り当てるのをお勧めします。
> その場合、Bootloaderキーは常設せず、ファームウェアをインストールする時だけ設定するのをお勧めします。

VialではBootloaderキーはQuantum Tabにあります。

> [!TIP]
> VialでBootloaderキーを設定しようとすると、Unlock Modeにするために2個のキーの長押しを指示する画面が出ますので、指示に従い2キーを長押ししてください。
> <p align="center"><img src="/images/inst_vial_bootloader.png" /></p>
> Vialでは、[Security]→[Reboot to bootloader]メニューからBootloaderモードにすることもできます。
> <p align="center"><img src="/images/inst_vial_bootloader_menu.png" /></p>

Remap版に戻したい場合は、[GreenkeysのFAQ](https://green-keys.info/gravity45-faq/#index_id29) を参照してください。

## Keymapの引き継ぎ方法

>[!IMPORTANT]
ファームウェアをインストールすると、KeymapがResetされるため、Keymapを引き継ぐにはインストール前に準備が必要です。

### A. Remapで設定したkeymapをVialでも引き継ぎたい場合

1. Remapでkeymapを保存してください。Google または Githubアカウントでのloginが必要です。  
    keymapを保存するには、画面右の[キーマップの保存・復元]メニューをクリックして、
    <p align="center">
      <img src="/images/reuseA_remap_save_menu.png" />
    </p>
    [現在のキーマップを保存]をクリックして、
    <p align="center">
      <img src="/images/reuseA_remap_save_keymap.png" />
    </p>
    任意の名前を入力して[保存]をクリックしてください。
    <p align="center">
      <img src="/images/reuseA_remap_save_button.png" />
    </p>
2. Vialファームウェアをインストールしてください。
3. Remapを開いてください。[Remap for QMK 0.18] を使うようメッセージが出るので、画面下の同リンクをクリックして、[START REMAP FOR YOUR KEYBOARD] をクリックしてください。
   <p align="center"><img src="/images/reuseA_remap_old_ver.png" /></p>
   <p align="center"><img src="/images/reuseA_remap_start.png" /></p>
4. 画面右の[Save/Restore a keymap]メニューから、1で保存したkeymapをクリックしてkeymapを読み込んで、[flash]をクリックしてください。
    <p align="center">
      <img src="/images/reuseA_remap_load_menu.png" />
      <img src="/images/reuseA_remap_load_keymap.png" />
      <img src="/images/reuseA_remap_load_flash.png" />
    </p>   

### B. Vialファームウェアを再インストール または 更新版をインストールした後でもkeymapを引き継ぎたい場合

1. Vial画面上で[File]→[Save current layout]メニューをクリックしてファイル保存してください。
   <p align="center"><img src="/images/reuseB_vial_save.png" /></p>
2. Vialファームウェアをinstallしてください。
3. Vial画面上で[File]→[Load saved layout]メニューをクリックして、1で保存したファイルを選択してください。
   <p align="center"><img src="/images/reuseB_vial_load.png" /></p>

## Vial の使い方

[Vial](https://get.vial.today/)から、[Start Vial Web]をクリックしてWeb版を使用するか、[Download Vial]をクリックしてアプリ版を使用してください。  
Vialの一般的な使用方法については、[Vialのドキュメント](https://get.vial.today/manual/) やWebを検索してください。

## 本ファームウェア独自の設定について

### Layer毎のRGB-LED

Gravity45は中央キーのみRGB LEDが搭載されています。本Vial対応ファームウェアでは、Layerを切り替えたら、RGB LEDの色が変更するようになっています。Caps Wordが有効な時も色が変更されます。  

**Q.Layer切替時にLEDの色が変更されない、または、Layer切替時にLEDの色を変更したくない**  
A.Toggle Keyを用意していますので、[Keymap]->[User]から[LTOG]を任意のキーに割り当てて、割り当てたキーを押して ON / OFF を切り替えてください。  
一度切り替えたら設定を保持していますので、不要でしたらキーの割り当てを外してください。

**Q.各Layerの色を自分で変更したい**  
A.[Keymap]->[User]に、Vial上で変更したLEDを設定するKey [LSAVE] を用意しています。色を変更したいLayerにした状態で、Vial上でLEDを設定してから [LSAVE] を押してください。  
また、Hue, Sat, Val (Brightness) の Up/Down Keyも用意しています。色を変更したいLayerに各キーを割り当てて押してください。  
尚、標準のBacklight Tabの[Hue+]などは、どのLayerに割り当ててもLayer 0の色だけに適用されます。

**Q.各Layerの輝度が変わらない**  
A.Defaultでは、Layer 0と同じ輝度が適用されるようにしています。  
Toggle Keyを用意していますので、[Keymap]->[User]から[LSMVAL (Layer Same Value)]を任意のキーに割り当てて、割り当てたキーを押して ON / OFF を切り替えてください。  
一度切り替えたら設定を保持していますので、不要でしたらキーの割り当てを外してください。

### OS毎のDefault Layer設定

OS毎にDefault Layerを設定できるようにしています。     
1. [Keymap]->[User]の[OSDF (OS Default Layer)]をDefault LayerにしたいLayerの任意のキーに割り当ててください。
2. OSにGravity45を接続してください。
3. 1で設定した[OSDF]キーを押してください。
4. Gravity45を再接続して、Default Layerが設定されたことを確認してください。

尚、QMKが対応しているWin, Mac, iOS, Linux, その他(Android含む)の分類を実装していますが、動作確認したのはMac, iOSのみです。

**Q.上記設定をリセットしたい**  
A.Reset Keyを用意していますので、[Keymap]->[User]から[MY_RST] を任意のキーに割り当てて、割り当てたキーを押してください。

## Source Code

本Vial Firmware用のソースコードは[こちら](https://github.com/karbou12/vial-qmk/tree/keyboard/gravity45/keyboards/green_keys/gravity_45/keymaps/vial)になります。  
Gravity45設計者のtakashicompany さんの [VIA用コード](https://github.com/takashicompany/qmk_firmware/tree/master/keyboards/green_keys/gravity_45)を元に作成しています。

##

>[!CAUTION]
>- 本ファームウェアに関して、Greenkeysさんのサポートはありません。開発者が分かる範囲でサポートしますが、基本的には自己責任でご利用ください。
>- Mac環境で作成し、Mac環境でのみ動作確認をしています。Windows環境でも初版の動作確認はしましたが保証はできません。
>- 本ファームウェアを使用したことによるいかなる損害についても、開発者は一切の責任を負いません。
