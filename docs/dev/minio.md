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
    - インストールとConfiguration
  - [AWS SDK for Javascript](https://docs.min.io/docs/how-to-use-aws-sdk-for-javascript-with-minio-server.html)
    - AWS SDKでminioを接続して操作可能
  - [Javascript Client api reference](https://docs.min.io/docs/javascript-client-api-reference.html)
    - minio client for js
    - minio serverとaws s3ともに使用できる（実行時の引数とかでわけれるかもね）
  - [AWS SDK for Python](https://docs.min.io/docs/how-to-use-aws-sdk-for-python-with-minio-server.html)
    - python用のAWS sdkであるboto3を用いてもminioを操作可能
  - [Python Client api reference](https://docs.min.io/docs/python-client-api-reference)
    - minio Library for python
    - ちょっとしたCLIツールに便利かも

### Webhook
  - [Introducing Webhooks for Minio](https://blog.minio.io/introducing-webhooks-for-minio-e2c3ad26deb2)
    - Thumbnail generatorでWabhookを使うさいの紹介