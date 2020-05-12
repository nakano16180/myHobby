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

## 参考リンク
### minio server
  - [minio/minio](https://github.com/minio/minio)
  - [LaravelからS3互換のMinIOを使えるように、docker-compose環境を整える](https://www.seeds-std.co.jp/blog/creators/2019-11-28-003000/)
  - [S3互換のオブジェクトストレージ MinioをDocker Composeで利用する](https://cloudpack-media.cdn.ampproject.org/v/s/cloudpack.media/46077/amp?usqp=mq331AQFKAGwASA%3D&amp_js_v=0.1#aoh=15851490530866&referrer=https%3A%2F%2Fwww.google.com&amp_tf=%E3%82%BD%E3%83%BC%E3%82%B9%3A%20%251%24s&ampshare=https%3A%2F%2Fcloudpack.media%2F46077)
  - [MinIO Server Config Guid](https://docs.min.io/docs/minio-server-configuration-guide.html)

### minio client
  - [MinIO Client Complete Guide](https://docs.min.io/docs/minio-client-complete-guide)
  - [JavaScript Client API Reference](https://docs.min.io/docs/javascript-client-api-reference.html)
  - [How to use AWS SDK for Javascript with MinIO Server](https://docs.min.io/docs/how-to-use-aws-sdk-for-javascript-with-minio-server.html)
  - [How to use AWS SDK for Python with MinIO Server](https://docs.min.io/docs/how-to-use-aws-sdk-for-python-with-minio-server.html)
  - [boto3でMinioのオブジェクトストレージにアクセスする(docker-compose)](https://qiita.com/th_/items/cf669949fe18f2eec5ab)
  - [AWS CLI with MinIO Server](https://docs.min.io/docs/aws-cli-with-minio)

### Notification
  - [Introducing Webhooks for Minio](https://blog.minio.io/introducing-webhooks-for-minio-e2c3ad26deb2)
  - [MinIO Bucket Notification Guide](https://docs.min.io/docs/minio-bucket-notification-guide.html)

### deploy
  - [Deploy MinIO on Docker Compose](https://docs.min.io/docs/deploy-minio-on-docker-compose.html)
  - [Deploy MinIO on Kubernetes](https://docs.min.io/docs/deploy-minio-on-kubernetes.html)
  - [Synology NASにMinio on DockerをインストールしてS3互換サーバーにする](https://blog.ik.am/entries/441)