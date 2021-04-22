# Zoom_auto : 群馬大学Zoom自動実行クライアント
授業時間になったらZoomに勝手に入ってくれるダメ人間製造機
___

### 現時点で入ってる機能
* 時間になったらZoomへ自動参加(5分前)
* 休日は勝手に認識して動かない
* 祝日及び日程変更で休日ができてもマニュアルで休日モードを変えられる
* 手動で指定した講義へ参加
* ハイブリッド授業形式に合わせて登校日は参加しない(新機能)


# 導入方法
![落とし方](https://github.com/ishida-shunya/Zoom_Auto/blob/images/image1.png)
はじめに、右上にある緑色の「code」ボタンをクリックし、下の方にある「Download Zip」を選択。
あとは好きなところに落としてあげて、Zipを展開すればダウンロード作業はおしまい。

#### Windows環境の方
落としたファイルの「Win_exe」フォルダーとその中身以外は消してもらって構いません。
「Win_exe」内の"群大Zoom自動実行.exe"をクリックすると起動します。

#### Macの方
製作者はMac環境で試せないので動く確証はありません。過去に動作確認を行いましたが、その後に色々手を加えてるので、動かなかったら諦めてください。
また、exeのようにパッケージ化してないので、Python導入→Python上でソースを動かす形になります。
参考にするのであれば[こういうの](https://daeudaeu.com/python-gui-install/#Python_Launcher_Python)かと。

### 授業ZoomID,パスワード及び説明の入力
起動する前に、授業情報の登録が必要です。授業情報は付属の`class.conf`に記入します。<br>
Win_exe側を使う方は「Win_exe」内部の`class.conf`を書き換えてください。<br>
メモ帳かなにかで開いてあげてると、こんな感じに書かれてます。

```
  [月曜日のID]
  1=aki
  2=aki
  3=aki
  4=aki
  5=aki
  [火曜日のID]
  ︙
  
  
  [月曜日のPass]
  1=
  2=
  ︙
  [火曜日のPass]
  ︙
  
  
  [月曜日の説明]
  1=なし
  2=なし
  ︙
  [火曜日の説明]
  ︙
  
```

ここの`[何曜日のID]`のところにZoomIDを空白無しで、`[何曜日のPass]`にはパスワードを入力しておきます<br>
また、空きコマのところには`aki`をつけておいてください。<br>
1は1-2限, 2は3-4限といった感じになってます。　1限単位での設定には対応していません。 <br>
### 書き方例

```
  [月曜日のID]
  1=90328874832
  2=90776543827
  3=aki
  4=96458250562
  5=aki
  [火曜日のID]
  ︙
  
  
  [月曜日のPass]
  1=663210
  2=003255
  3=
  4=997600
  5=
  [火曜日のPass]
  ︙
```

![こんな感じで出るよ](https://github.com/ishida-shunya/Zoom_Auto/blob/images/image2.png)

一番下の`[何曜日の説明]`になにか書いておくと、Zoom参加時にメッセージが表示されます。出席確認がMoodleで行われるとか、カメラOnの準備をする！　みたいなちょっとした情報を書いておくのに使ってください



### フォントの導入(任意)
本アプリでは標準フォントとしてM+ 2pを選択しています。このフォントを入れてもらうとよりきれいなレイアウトになります。
https://mplus-fonts.osdn.jp/about.html

# 使い方 & 操作説明
基本的には起動して放置しとけばいいけど、一応解説。

![起動画面](https://github.com/ishida-shunya/Zoom_Auto/blob/images/image3.png)<br>
起動するとこんな感じの画面が開きます。
右上の「休日モードにする」をONにすることで、OFFにするまでZoomに入らなくなります。　休校日とか祝日のときに使ってください
また、下の画像でおおよその状態がわかります。(しばらくなにもない, 講義直前, 講義中, 登校日など)

上の「設定」タブを押すことで、設定画面が開きます。

![設定画面](https://github.com/ishida-shunya/Zoom_Auto/blob/images/image4.png)<br>
* **休日モードが一日で切れるようにする**
　<br>休日モードがある時間に自動で切れるようになります。気づかないまま寝落ちして次の日に寝坊するのを防止する用の機能。
* **休日モードを外す時間**
  <br>一応変更できます。　こだわりの多い方はぜひどうぞ。
* **学籍番号設定(ハイブリッド用)**
  <br>設定するとハイブリッド授業に対応し、登校日はZoomが起動しない設定になります。`設定なし`なら常に起動します。
* **マニュアル実行**
  <br>任意の時間の講義に手動で参加します。　授業変更などでお使いください
  
### マニュアル実行のやりかた
* 曜日欄と時限欄をそれぞれ合わせる
* 設定できたら「実行」をクリック！

# 注意
ステータス表示はガバガバ制御なので当てになりません。
<br>(Zoom の実行と設定画面はちゃんと動く、、、はず)

あくまでも出席するだけなので目覚まし機能とかはありません。頑張って起きてください

ハイブリッド授業機能は半分おまけみたいなもんなので変則日程には対応してません。

画像は著作権ガン無視で使ってるのでうん、やばいかも

Mac ではレイアウトが崩れます。仕様です

# 連絡先
t200d005@gunma-u.ac.jp
