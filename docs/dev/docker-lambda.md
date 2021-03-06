## docker-lambda
[コード](https://github.com/lambci/docker-lambda)

"stay-open" API modeが便利

立ち上げは以下のコマンド。これでローカルにlambdaのサーバーを立てることができる。

```
$ docker run --rm [-d] \
  -e DOCKER_LAMBDA_STAY_OPEN=1 \
  -p 9001:9001 \
  -v <code_dir>:/var/task:ro,delegated \
  [-v <layer_dir>:/opt:ro,delegated] \
  lambci/lambda:<runtime> \
  [<handler>]
```

ターミナルに以下を入力してサーバーが立っていることを確認できる
```
$ curl -d '{}' http://localhost:9001/2015-03-31/functions/myfunction/invocations
```

自分で作ったアプリなどと合わせて使う場合は上記urlにデータを投げると良い

## 参考リンク
  - [サンプルコード](https://github.com/lambci/docker-lambda/blob/master/examples/python/lambda_function.py)
  - [チュートリアル: Amazon S3 で AWS Lambda を使用する](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/with-s3-example.html)
    - IAMロールの作成
    - バケット作成
    - 関数の作成
    - デプロイパッケージの作成（AWS CLIでアップロード）
    - AWS S3の設定とイベント発行
  - [サンプル Amazon S3 関数コード](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/with-s3-example-deployment-pkg.html)
  - [Amazon S3 イベントでの AWS Lambda の使用](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/with-s3.html)
  - [docker-lambda を使って AWS Lambda Function を開発する方法](https://r17n.page/2019/08/18/aws-docker-lambda-usage/)
  - [docker-lambda - AWS Lambda の開発効率を爆アゲする](https://qiita.com/anfangd/items/bb448e0dd30db3894d92)
  - [AWS Lambda(Node.js) + ffmpeg でエンコード](https://xp-cloud.jp/blog/2018/05/18/3345/)