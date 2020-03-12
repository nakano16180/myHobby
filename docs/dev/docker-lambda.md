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