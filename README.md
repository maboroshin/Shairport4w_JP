## Shairport4w 日本語化

[Shairport4w](https://github.com/Frank-Friemel/Shairport4w) の日本語化です。バージョン1.0.9.5(2022年)で公式サイトのプログラムが日本語化されています。iPhoneやiTunesなど、AirPlayに対応したApple製品の音声をパソコン側で受信して再生できます。何年も開発していない様子。

* [Readme.txt](https://sourceforge.net/projects/shairport4w/files/) なぜか1.0．8.8まで（GitHub以降以前のsourceforgeに存在）

## 接続方法
パブリックに設定されたネットワークでは、初回起動時に、ファイヤーウォールの設定が出るので「パブリック」を許可する必要があるみたいです。プライベートに設定されたネットワークではファイアウォールは不要かも。この接続がうまくいけば、送信先の AirPlay のマークを押した時に、パソコンが候補に表れます。

## 既存のバグ

* トレイに再生中を表示できない
* https://github.com/Frank-Friemel/Shairport4w/issues/5 : サウンドカードので出力デバイスの変更ができない（2020年の情報では古いバージョン1.0.8.8に戻すと再生できる）
* https://github.com/Frank-Friemel/Shairport4w/issues/7 : 自動起動できません

1.0.9.6用の文字切れの変更点はここ (ResourceHackerで変更してください) :  https://github.com/Frank-Friemel/Shairport4w/pull/28/files

### 日本語化方法の解説
（公式サイトのプログラムが日本語化されたので古い記述です。）

[ResourceHackerPortable](https://portableapps.com/apps/utilities/resource-hacker-portable)で追加してください。 [ResourceHacke 日本語化ファイル](https://github.com/Rukoto/Toy-Box)または[日本語化2](https://wwwcfe.hatenablog.com/entry/20100917/resourcehacker) （この日本語化ファイルは App\ResourceHacker\ResourceHacker.exe と同じフォルダに置きます）

Resource Hacker で出力された ```[Shairport4w.1.0.9.4.rc](https://github.com/maboroshin/Shairport4w_JP/raw/master/Shairport4w.1.0.9.4.rc)``` （削除してあります）を読み込みます（削除したけどコミットの履歴から表示もできます）。メニューの「操作」（Action）から、「スクリプトをコンパイル」（Compile Script F5）、そしてバイナリ RES (```.res```) で保存します。Resource Hacker で実行ファイル ```Shairport4wx64.exe``` （64ビット版の場合）を読み込み、「操作」の「リソース ファイル (*.res 略)から追加(R)」で、今バイナリにしたこの ```.res``` を追加します。ダイアログが出るので、「上書き」（Overwrite）と「すべて選択」（Check）を選択し、インポート（Import）、そして保存します。

## ライセンス
Shairport4w は、オープンソースの GPL3.0 のライセンスになっているので、これを継承しています。
