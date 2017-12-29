# Adam Smith説明書
作成日：2017.12.03
更新日：2017.12.24

![Adam Smith](https://upload.wikimedia.org/wikipedia/commons/1/18/37.Adam_Smith.jpg "Adam Smith")

## Adam Smithとは
アダム・スミスとは、「神の見えざる手」によりユーザにとって
役に立つ情報を教えてくれたり必要な情報をストックしてくれたりするLine Botの事です。
アダム・スミスの機能を以下に示します。

* ヘルプ
* 電車の遅延情報登録/通知
* アダム・スミス返答登録
* 家計簿
* 天気情報
* リマインダー
* タイマー
* 星座占い

## 対象者

* 朝出勤前に電車の遅延情報をLineで通知してほしい方
* 朝出勤前にその日の天気状況に応じて傘の有無を教えてほしい方
* 「彼女の誕生日」を忘れて、当日怒りの鉄槌が落ちるのを回避したい方

<a href="https://line.me/R/ti/p/%40lul2727q"><img height="36" border="0" alt="友だち追加" src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png"></a>

## 使い方

### ヘルプ

以下のメッセージをアダム・スミスに送ると、アダム・スミスのマニュアル（本ページ）のURLが表示されます。

```
ヘルプ

or

help
```

### 電車遅延通知
関東圏に限り、ユーザの登録情報に従い任意の電車の遅延情報を教えてくれます。
時間指定（範囲指定）で通知するタイミングが設定可能です。

#### 通知設定方法
以下のようにアダム・スミスにメッセージを送ってください。

コマンド
```
登録 電車 [通知してほしい電車] [通知開始時刻] [通知終了時間]

```
| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 通知してほしい電車 |電車名を記載する。注意点として正式名でないと登録できない。|
| 通知開始時刻 |電車の遅延情報が何時から欲しいかを登録する。数字0-23で登録する|
| 通知終了時刻 |電車の通知終了時刻が何時から欲しいかを登録する。数字0-23で登録する |



例）東海道本線遅延情報を午前7時-14時まで通知してほしい場合

```
登録 東海道本線[東京～熱海] 7 14
```
例）山手線遅延情報を午後15-18時の間通知してほしい場合
```
登録 電車 山手線 15 18

```
#### 登録されている電車の遅延情報を表示する
以下のようにアダム・スミスにメッセージを送ってください。
```
登録 電車
```

#### 登録可能電車一覧を表示
以下のようにアダム・スミスにメッセージを送ってください。

```
登録 電車 一覧

```

#### 登録されている電車の遅延情報を削除する
以下のようにアダム・スミスにメッセージを送ってください。
```
削除 電車 [登録ID]
```
※ [登録ID]は登録 電車コマンドを入力した際に出力されます。


### アダム・スミス返答登録
アダム・スミスがアタナに返す返答を登録することができます。

コマンド
```
登録 メッセージ [フィルターする言葉] [アダム・スミスの返答]
```
| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| フィルターする言葉 |この言葉が来たら[アダム・スミスの返答]があなたに返されます|
| アダム・スミスの返答 |アダム・スミスがあなたに返す言葉|


登録例）辛いとつぶやいたらアダム・スミスに頑張って！と言ってもらいたい場合
```
登録 メッセージ 辛い 頑張って！
```


### 家計簿
以下のようにアダム・スミスにメッセージを送って下さい。

#### 家計簿に登録したい場合

```
[値段（必須）] [物の名前（必須）] [メモ（任意）]
```
| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 値段 |300円のように、円表記で登録する。万や千表記には対応していない。1万円の場合も、10000円として登録する。|
| 物の名前 |購入したものの名前を任意に登録する|
| メモ |必須ではない。購入に関するメモを登録する。 |


登録例1）メモを取った場合の登録例

```
150円 お茶 外出先で購入
```

登録例2)メモを取らない場合の登録例

```
1000円 化粧品
```

#### 家計簿に登録した情報を見たい場合

```
家計簿 一覧　[期間（任意）]
```
| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 期間 |１週間 or w と入力すると1週間分の家計簿一覧が出力される。入力しない場合は今まで購入したもの全てを表示|

例1）家計簿に登録された商品の一覧を見たい場合

```
家計簿 一覧
```

例2) 家計簿に登録された1週間分の商品の一覧を見たい場合

```
家計簿 一覧 w
```

#### 家計簿合計

今までの合計を出力したい場合は以下のコマンドを入力

```
家計簿 合計
```


### 天気情報通知

#### 天気情報登録

```
登録 天気 [都市名] [通知したい時間]
```
| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 都市名 |天気情報を取得したい都市名を漢字かアルファベットで入力する。 例）yokohama or 横浜|
| 通知したい時間 |0-23 の数字を入力する。例） 9|

例）鎌倉の天気予報を午前7時に知りたい場合

```
登録 天気 鎌倉 7
```

#### 登録天気情報一覧を取得
以下のようにアダム・スミスにメッセージを送る。

```
登録 天気
```

#### 登録天気情報の削除
以下のようにアダム・スミスにメッセージを送る。

```
削除 天気 [登録ID]
```

| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 登録ID | "登録 天気" コマンドで取得したIDの事。|

例）登録IDが3の登録情報を削除する場合

```
削除 天気 3
```


### リマインダー

```
リマインダー [思い出させたいこと] [月] [日] [時] [分]
```

| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 思い出させたいこと |通知させたいことを任意に入力  |
| 月 | 1-12の数字を入力する　例）12  |
| 日 | 1-31の数字を入力する　例）30  |
| 時 | 0-23の数字を入力する　例）3  |
| 分 | 0-59の数字を入力する　例）58  |

登録例） 12/25 15:00 に会社の会議を思い出させたい場合
```
リマインダー 会社の会議 12 25 15 0
```

### タイマー

```
タイマー [時間]
```
※1時間以内

| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 時間              |時間、分、秒で時間指定する 例）タイマー 30秒   |



### 星座占い

あなたの星座をアダム・スミスにメッセージとして送って下さい。
注意点として、すべての星座は"漢字"で入力して下さい。

例）
```
蠍座
```
