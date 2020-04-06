[公式ドキュメント](https://docs.masoniteproject.com/)

## Masonite tutorials

  - [公式チュートリアル](https://docs.masoniteproject.com/creating-a-blog)

```
$ mkdir masonite_tutorial
$ cd masonite_tutorial/
$ virtualenv -p python3.6 .venv
$ source .venv/bin/activate

$ pip3 install masonite
$ craft new
$ craft serve

```

ブログを作った。  
ルーティングは以下のようになっている。

  - http://localhost:8000
  - http://localhost:8000/register
  - http://localhost:8000/login
  - http://localhost:8000/home
    - blogへのリンクほしい
  - http://localhost:8000/blog
    - 「Post!」を押すと/blog/createにpostされ、/blog/postにリダイレクト
  - http://localhost:8000/blog/crate
  - http://localhost:8000/posts
    - 投稿一覧画面
  - http://localhost:8000/post/1
    - 投稿の詳細ページ
    - 投稿一覧からリンクしたい
  - http://localhost:8000/post/1/update
    - 投稿をupdate or delete
    - 投稿の詳細ページからリンクしたい

### 発展
- [Introduction to Masonite and VueJS](https://medium.com/swlh/introduction-to-masonite-and-vuejs-e8538064a054)
    - Masonite tutorialsのブログを作りつつフロントにVueJSを使う方法

## デプロイ
  - [Deploying a Masonite Application to Heroku](https://dev.to/masonite/deploying-a-masonite-application-to-heroku-45jp)
  - [Masonite をHerokuで公開する方法](https://qiita.com/kentaro0919/items/8ac362d1596d3cdc212f)

## リンク集
  - [Masonite-with-Postgres](https://testdriven.io/blog/dockerizing-masonite-with-postgres-gunicorn-and-nginx/#.XlJ_GULrcz8.twitter)
    - masoniteアプリをDockerで立ち上げ
    - 使用するデータベースをPostgreSQLに設定
  - [Masonite Logging](https://docs.masoniteproject.com/official-packages/masonite-logging)
    - ログ機能の追加
    - slackにログを投げたりできて便利そう
  - [Masonite Notifications](https://docs.masoniteproject.com/official-packages/masonite-notifications)
    - メールかslackに通知を送る機能
  - [masonite-app-with-user-verification](https://github.com/nioperas06/masonite-app-with-user-verification)
    - masoniteとjson web tokenでメール認証機能を作れるっぽい
