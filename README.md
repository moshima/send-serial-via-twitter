# TwitterのユーザーにDMを送信する

## 使い方

### インストール

```
git clone REPOSITORY
bundle install --path vendor/bundle
```

### 設定

```
bundle exec t authorize
```

1. Twitterの開発者ページ https://dev.twitter.com/apps にログイン
2. Create a new application をクリック
  * Name : USER/t
  * その他必須項目を入力
3. OAuth settings のパラメータを t に設定
  * consumer key
  * consumer secret
4. Twitterアプリとしてtを認証
  * 表示されたURLにアクセス (https://api.twitter.com/oauth/authorize?...)
  * 連携アプリを認証
  * 表示されたPINをtに入力
5. 認証状況の確認
  ```
bundle exec t accounts
USER
  7uyX0g16ZB2YkbPweah8I (active)
  ```
6. SettingsタブのApplication Typeを"Read, Write and Access direct messages"にする



## t の使い方

### DM を送る

```
bundle exec t dm USER MESSAGE
```


## Twitterの制限

https://support.twitter.com/articles/249071-twitter-apidm

* ダイレクトメッセージ：250件／1日


