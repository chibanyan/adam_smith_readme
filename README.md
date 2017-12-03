# Adam Smith説明書
作成日：2017.12.03
更新日：2017.12.03

![Adam Smith](https://upload.wikimedia.org/wikipedia/commons/1/18/37.Adam_Smith.jpg "Adam Smith")

## Adam Smithとは
アダム・スミスとは、「神の見えざる手」によりユーザにとって
役に立つ情報を教えてくれるLine Botの事です。
アダム・スミスは以下の情報を教えてくれます。

* 電車の遅延情報
* 天気情報
* リマインダー

## 対象者

* 朝出勤前に電車の遅延情報をLineで通知してほしい方
* 朝出勤前にその日の天気状況に応じて傘の有無を教えてほしい方
* 「彼女の誕生日」を忘れて、当日怒りのボルテージが落ちるのを回避したい方

## 使い方

### 電車遅延通知
関東圏に限り、ユーザの登録情報に従い任意の電車の遅延情報を教えてくれます。
曜日指定、時間指定（範囲指定）で通知するタイミングが設定可能です。

#### 通知設定方法
以下のようにアダム・スミスにメッセージを送ってください。

コマンド
```
t: [通知してほしい電車] [通知日] [通知時間]
or 
train: [通知してほしい電車] [通知日] [通知時間]

```
| コマンドオプション | 意味                                         |
|:------------------|----------------------------------------------:|
| 通知してほしい電車 |電車名を記載する。例）東海道線 |
| 通知日 |平日、全日のどちらか|
| 通知時間 |範囲を指定する場合は「-」、それ以外は数字を入力 |



例）東海道線遅延情報を平日午前7時-14時まで通知してほしい場合

```
:t 東海道線 平日 7-14
```
例）山手線遅延情報を全日（土日を含むすべての日）午前8時、10時、午後15-18時の間通知してほしい場合
```
:t 山手線 全日 8,10,15-18
```


### 天気情報通知

実装中。
乞うご期待


### リマインダー

実装中。
乞うご期待

### 家計簿

実装中。
乞うご期待

### 星座占い

あなたの星座をアダム・スミスにメッセージとして送って下さい。
注意点として、すべての星座は"漢字"で入力して下さい。

例）
```
蠍座
```
