## 問題名

設定が保存できない

## 概要

`router` の設定ファイルをTFTPで `server` に保存したい。
しかし、何故か分からないが `server` に保存しようとするとエラーが発生する。
`router` から `server` にTFTPで設定ファイルを送信し、その方法を教えてほしい。

## 前提条件

- 設定はTFTPで転送しなければならない
- 設定内容をターミナルに出力することは認められる
- 報告書は操作内容や状況を逐一詳細に記さなければならない
    - 特に、制約に反していないこと、終了状態が満たせていることを明確に示すこと

### 制約

- `router` の設定をTFTP以外の手段で転送してはならない
- ターミナルに出力した設定内容を、設定内容の確認以外に用いてはならない
    - 確認した内容をファイルに書き込むなどの回答は認められない
- TFTPで転送したファイルに対して、移動、名前変更その他の改変を加えてはならない

## 初期状態

- `router` のconfiguration modeで `save tftp://192.168.96.2/config` としても `server` に設定ファイルを保存できない

## 終了状態

- `router` のconfiguration modeで `save tftp://192.168.96.2/config` とすると `server` に設定ファイルを保存できる
- `server` に保存された設定ファイルが回答時点での `router` の設定と同一であること
    - 設定ファイルの内容が初期状態と異なっていても問題ない

## 接続情報

| ホスト名 | IPアドレス | ユーザ | パスワード|
| --------- | ----------- | ------ | ------------------ |
| `router` | 192.168.96.1 | user | ictsc |
| `server` | 192.168.96.2 | user | ictsc |
| `server` | 192.168.52.128 | worker |  |
