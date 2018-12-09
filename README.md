# mail2typetalk
Mail to Typetalk with Mailgun API/GAE

# 使い方
secret.yaml.sampleを参考に、secret.yamlを準備。

* MAILGUN_API_KEY
  * MailgunのAPIキー
* TYPETALK_CLIENT_ID
  * TypetalkはClient CredentialをつかったAccessTokenでアクセスするため、CLIENT IDを設定。
  * CLIENT IDの取得等は[Typetalk APIドキュメント](https://developer.nulab-inc.com/ja/docs/typetalk/auth/#client)を参照。
* TYPETALK_BOT_POST_URL
  * エラー時のメッセージなどをTypetalkに投稿するためのBOT用POST URL設定。
    * こちらは上記CLIENT IDとは別で、トピック内でBOTを作成してそのURLを設定。
  * 専用のトピックを作って管理者だけが見れるようにしておくのが想定。
* GOOGLE_APPLICATION_CREDENTIALS
  * Cloud Datastoreを使うための認証用ファイル。Google Cloudで生成されたjsonファイルを指定。
* CLOUD_STORE_KIND
  * Datastore上のkind 特に指定はないので、任意の名前でOK。

その上で、
```bash
$ python3 -m venv env
$ source env/bin/activate
$ pip install -r requirements.txt
$ python main.py
でローカルでサーバが起動できる。可能であれば、このサーバにMailgunからのPOSTが届くようにすればテストしやすい。

GAEへのデプロイなどは、GAEドキュメントを参照。
