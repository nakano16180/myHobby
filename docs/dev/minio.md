## Object storage for Local
- ローカルで構築できるAWS S3互換のオブジェクトストレージ  
- 後述のクライアントツールmcの他、AWS CLIで操作することも可能
- 自作アプリでS3使いたいけど課金が心配などの場合に気にせず使える

### Minio

[公式ドキュメント](https://docs.min.io/)

```
$ docker pull minio/minio
$ docker run -p 9000:9000 minio/minio server /data
```

### mc(Minio Client)

Minio serverのセットアップ用CLIツール

```
$ docker run -it --entrypoint=/bin/sh minio/mc
```

### その他SDK
  - [AWS CLI](https://docs.min.io/docs/aws-cli-with-minio)
  - [AWS SDK for Javascript](https://docs.min.io/docs/how-to-use-aws-sdk-for-javascript-with-minio-server.html)
  - [Javascript Client api reference](https://docs.min.io/docs/javascript-client-api-reference.html#getBucketNotification)
  - [Python Client api reference](https://docs.min.io/docs/python-client-quickstart-guide)