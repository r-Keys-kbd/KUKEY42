# ビルドガイド

## 0. 準備
### 内容物
内容物がそろっていることをご確認ください。
|品名|数量|備考|
|---|---|---|
|メイン基板|1セット||
|Kailh Switch Socket|44個|ロープロファイル用 予備2個|
|ダイオード|42個|ハンダ済|
|スライドスイッチ|2個|ハンダ済 JS102011SAQN|
|リセットスイッチ|2個|ハンダ済 SKSCLDE010|
|JST1.25mmバッテリーコネクタ|2個|ハンダ済 1.25-2PWB|
|水平ロータリーエンコーダ（クリック付き）|1個|[THQWGD001C](https://tarohayashi.booth.pm/items/5967252) [^1] |
|BLEマイコン|2個|ハンダ済 Seeed Studio XIAO nRF52840|
|7ピンL字コンスルー|1個||
|トラックボール読取り基板|1個||
|トラックボールセンサ|1個|PMW3610DM|
|トラックボールセンサレンズ|1個||
|トッププレート|1セット|アルミ|
|トップケース|1セット|3Dプリンタ製|
|ボトムケース|1セット|3Dプリンタ製|
|ネオジウム磁石 D10×2mm|10個|ボトムケース用|
|M2×2.5mm 低頭精密小ねじ|8個||
|樹脂スペーサー 6mm|8個||
|M2×5mmプラスチックネジ|8個|トッププレート固定用|
|25mmトラックボールケース|1個|3Dプリンタ製|
|ベアリング|3個|取り付け済 681XZZ|
|M1.4×5mm なべ小ねじ|3個|取り付け済|
|M1.7×5mm 低頭精密小ねじ|2個|トラックボールケース取付用|
|ポロンシート|2枚||
|滑り止めシール|8枚|+GRIPLUS+|

### ご準備いただく物
|品名|数量|備考|商品例|
|---|---|---|---|
|キースイッチ|42個|ロープロファイル用(Choc V2系)|[Hades Low-profile Switches](https://www.lofree.co/products/hades-low-profile-pom-switches)|
|キーキャップ|42個|17mmピッチ対応品|[Kotori Blank(Proto)](https://booth.pm/ja/items/6781056)|
|25mmトラックボール|1個||[M-B25RD](https://www.elecom.co.jp/products/M-B25RD.html)|
|リチウムポリマーバッテリー|2個|厚さ4mm以下、JST1.25mmコネクタ|[Amazonリンク](https://www.amazon.co.jp/dp/B0FBW68HQP)|

### 組立てに必要な道具
|品名|備考|
|---|---|
|はんだ付けセット|私は[Kz流はんだ付け](https://note.com/kazu_dob/n/nd0040b07fc6e)を見て、自分に必要そうな物を買いました|
|ドライバー|M2には#1、M1.7には#0が適している|
|ピンセット||
|マスキングテープ|はんだ付け時の部品固定に|
|ペンチ||


## 1. 半田付け
### 1.1. メイン基板
半田付け完了した状態が下記ですので、完成図を見ながら、半田付けをするとミスを減らせると思います。\
<img src="./img/PCB_1.jpg" width=480>  <img src="./img/PCB_2.jpg" width=480>

#### 1.1.1. キーソケット
　(1) 片側のパッドに半田を盛る\
　　<img src="./img/Keysocket_1.jpg" width=240>  <img src="./img/Keysocket_2.jpg" width=240>  <img src="./img/Keysocket_3.jpg" width=240>

　(2) 基板のプリントの形に合わせて、キーソケットを配置する\
　　<img src="./img/Keysocket_4.jpg" width=360>

　(3) 半田を溶かしながら、ピンセットで軽く押さえて、基板とソケットをくっつける\
　　<img src="./img/Keysocket_5.jpg" width=360>

　(4) 反対側も半田付けを行う

　(5) 最初に半田を盛った側も必要に応じて、半田を追加し、形を整える（フラックスを塗ると整えやすい）

#### 1.1.2. 7ピンL字コンスルー
　(1) キーソケットが付いている面と逆側から<ins>直線のピン</ins>を穴に通し、マスキングテープ等で固定する\
　　<ins>※取付面を間違えやすいので、要注意</ins>\
　　<img src="./img/7pin_1.jpg" width=360>

　(2) 両端の2か所だけ半田で仮止めし、基板とコンスルーに隙間がないことを確認する\
　　隙間がある場合は、基板を水平に浮かせて、仮止め個所をコテで温めて、調整する

　(3) 問題がなければ、すべてのピンを半田付けする

#### 1.1.3. ロータリーエンコーダ
　(1) [THQWGD001Cのビルドガイド](https://github.com/Taro-Hayashi/THQWGD001/blob/main/assemble_c.md)を参照し、キーソケットが付いている面と逆側にロータリーエンコーダを取り付ける\
　　<ins>※ビルドガイドでは付属のボトムプレートに取り付けておりますが、ボトムプレートは不要です。直接基板に取り付けてください</ins>\
　　<img src="./img/Encoder_1.jpg" width=360>

　(2) エンコーダの足（3本）とスイッチの足（4本）を半田付けする

### 1.2. トラックボール読取り基板

半田付け完了した状態が下記ですので、完成図を見ながら、半田付けをするとミスを減らせると思います。\
<img src="./img/TB_PCB_1.jpg" width=360>  <img src="./img/TB_PCB_2.jpg" width=360>

　(1) トラックボールセンサを基板に取り付ける\
　　<ins>※部品の向き、取付面に気を付ける</ins>

　(2) 対角になるように2か所だけを半田で仮止めする

　(3) 基板とセンサに隙間がある場合、センサを押さえつけながら、仮止めした半田を溶かして、調整する

　(4) 問題がなければ、すべてのピンを半田付けする\
 ※間隔が狭いため、ブリッジしないように気を付ける</ins>\
　　<img src="./img/TB_PCB_3.jpg" width=360>

　(5) センサの保護シールをはがし、レンズを取り付ける\
　　<img src="./img/TB_PCB_4.jpg" width=360>

## 2. ケース組立て
　(1) トップケースの六角スペーサを取付け用の台にはめて、裏側からねじ止めする（片側4か所）\
　　<img src="./img/Case_1.jpg" width=360>  <img src="./img/Case_2.jpg" width=360>

　(2) トップケースの溝にボトムケースの爪がハマる構造となっています\
　　下側（USB口の反対側）をはめて、上から押さえて、少しずつはめてください\
　　<ins>※力を入れすぎるとケースが破損する恐れがありますため、固い場合、一度外して、再度、押さえてみてください</ins>\
　　<img src="./img/Case_3.jpg" width=360>  <img src="./img/Case_4.jpg" width=360>

　(3) ボトムケースを外す場合、USB口に指を入れて、トップケースを持ち上げるようにしてください\
　　<ins>※ケースの細い部分は持たないようにしてください。破損の恐れがあります</ins>\
  　<img src="./img/Case_10.jpg" width=360>
   
　(3) リセットボタンを内側から入れる\
　　<ins>※リセットボタンは裏表があり、少しだけ辺が短い方をケースの外側になるようにしてください</ins>\
　　<img src="./img/Case_5.jpg" width=240>  <img src="./img/Case_6.jpg" width=240>  <img src="./img/Case_7.jpg" width=240>
  
　(3) ネオジウム磁石をはめてください\
 　　<ins>※左右のケースの磁極を逆にすることで、重ねると磁力でくっつくようになります</ins>\
   　<img src="./img/Case_8.jpg" width=360>
 
　(4) トップケースの中にポロンシートを敷く\
　　<img src="./img/Case_9.jpg" width=360>
  
　(5) バッテリーを接続する前に電源がOFFになっていることを確認してください\
　　<ins>※左右両方とも下がOFFです</ins>\
　　<img src="./img/PowerSwitch_1.jpg" width=360>
  
　(6) バッテリーを接続する\
　　<ins>※基板のプラス側が赤線十なっていることを確認してください。たまに極性が逆の場合があります</ins>\
　　<img src="./img/Battery_1.jpg" width=360>
  
　(7) トップケースの中に基板を入れる\
  　<ins>※リセットスイッチが引っ掛かりやすいので、気を付けてください</ins>\
　　<img src="./img/Case_11.jpg" width=360>  <img src="./img/Case_12.jpg" width=360>
  
　(8) トッププレートをかぶせて、六角スペーサの位置でねじ止めする\
　　<img src="./img/Case_13.jpg" width=360>

　(9) 7ピンL字コンスルーにトラックボール読取り基板を取り付ける（半田付け不要）\
　　<img src="./img/TB_PCB_5.jpg" width=360>
  
　(10) お好みで、滑り止めをマグネットが見えなくなるように貼り付ける


## 3. ファームウェア
### 3.1. ファームウェアのダウンロード
　(1) [ファームウェアのリポジトリ](https://github.com/r-Keys-kbd/zmk-config-KUKEY42)にアクセスする
 
　(2) "Actions"タブを開く\
　　<img src="./img/FirmwareDL_1.jpg" width=480>

　(3) 最新のWorkflowを開く\
　　<img src="./img/FirmwareDL_2.jpg" width=480>

　(4) ArtifactsのFirmwareをクリックするとダウンロードが開始される\
　　<img src="./img/FirmwareDL_3.jpg" width=480>

　(5) ダウンロードしたZIPファイルには下記3つのファイルが入っている
|ファイル名|備考|
|---|---|
|KUKEY42_L rgbled_adapter-seeeduino_xiao_ble-zmk.uf2|左側用ファームウェア|
|KUKEY42_R rgbled_adapter-seeeduino_xiao_ble-zmk.uf2|右側用ファームウェア|
|settings_reset-seeeduino_xiao_ble-zmk.uf2|リセット用ファームウェア|
   

### 3.2. リセット用ファームウェアの書込み
　(1) PCとマイコンをUSB Type-Cケーブルで接続する
  
　(2) ボトムプレートを外し、マイコンがある位置の左側の穴に爪楊枝等を挿して、マイコンのリセットボタンをダブルクリックする
  
　(3) 「XIAO SENSE」ドライブのエクスプローラーが開くので、リセット用ファームウェアをドラッグアンドドロップする

　(4) 「XIAO SENSE」ドライブのエクスプローラーが自動で閉じたら、書き込み完了

　(5) 反対側のマイコンも同様の手順で書き込みを行う

### 3.3. ファームウェアの書込み
　(1) PCと右側のマイコンをUSB Type-Cケーブルで接続する

　(2) "リセット用ファームウェアの書込み"と同様の手順で「XIAO SENSE」ドライブのエクスプローラーを開き、右側用ファームウェアをドラッグアンドドロップする

　(3) 「XIAO SENSE」ドライブのエクスプローラーが自動で閉じたら、書き込み完了

　(4) 左側のマイコンも同様の手順で書き込みを行う\
 　　<ins>※書き込むファームウェアは左側用を使用する</ins>

## 4. キーマップカスタマイズ
### 4.1. 専用リポジトリの作成
　(1) 自身のGitHubアカウントでログインする\
　　※（アカウントを持っていない場合、[公式サイト](https://docs.github.com/ja/get-started/start-your-journey/creating-an-account-on-github)の手順に沿って作成する）

　(2) [ファームウェアのリポジトリ](https://github.com/r-Keys-kbd/zmk-config-KUKEY42)にアクセスする

　(3) 画面右上の「Fork」をクリックする\
　　<img src="./img/Firmware_1.jpg" width=480>

　(4) 設定は変更せずに、"Create fork"をクリックする\
　　<img src="./img/Firmware_2.jpg" width=480>

　(5) フォークしたリポジトリの"Actions"タブをクリックする\
　　<img src="./img/Firmware_3.jpg" width=480>

　(6) "I understand my workflows, go ahead and enable them"をクリックし、github Actionsを有効化する\
　　<img src="./img/Firmware_4.jpg" width=480>

### 4.2. KeymapEditorの場合
　(1) [KeymapEditor](https://nickcoutsos.github.io/keymap-editor/)にアクセスする

　(2) "GitHub"を選択し、"Login with GitHub"をクリックする\
 　　<img src="./img/KeymapEditor_1.jpg" width=480>

　(3) "Authorize Keymap Editor"をクリックする\
 　　<img src="./img/KeymapEditor_2.jpg" width=480>
   
　(4) "Add Repository"をクリックする\
 　　<img src="./img/KeymapEditor_3.jpg" width=480>
   
　(5) "Only select repositories"をクリックする\
　(6) "Select repositories"でForkした"zmk-config-KUKEY42"を選択する\
　(7) "Install"をクリックする\
 　　<img src="./img/KeymapEditor_4.jpg" width=480>
   
　(8) 自分好みにキーマップをカスタマイズしたら、Saveする\
 　　<img src="./img/KeymapEditor_5.jpg" width=480>

　(9) 自動でFirmwareのビルドが開始されるので、完了したら、デフォルトのFirmwareと同様の手順でダウンロードする
 
### 4.3. ZMK Studioの場合
　(1) [ZMK Studio](https://zmk.studio/)にアクセスする

　(2) トラックボール側のキーボードをUSBで接続する

　(3) "USB"をクリックする

　(4) "KUKEY42"を選択して、"接続"をクリックする

　(5) キーマップをカスタマイズする

　(6) 右上のSaveボタンをクリックする 

## 脚注
[^1]:はやしたろうさん製 [ショップページ](https://tarohayashi.booth.pm/).
[^2]:roBa [製品ページ](https://booth.pm/ja/items/6010869?srsltid=AfmBOopq70Ue1cWkGQTA1_aS9Vm7guz2w68s4GnI2Vtczi-fyKXTgD8y)

