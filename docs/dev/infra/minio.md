## Minio 
  - ローカルで構築できるAWS S3互換のオブジェクトストレージ  
  - 後述のクライアントツールmcの他、AWS CLIで操作することも可能
  - 自作アプリでS3使いたいけど課金が心配などの場合に気にせず使える

### minio server

[公式ドキュメント](https://docs.min.io/)
[minio/minio](https://github.com/minio/minio)


```
$ docker pull minio/minio
$ docker run -p 9000:9000 minio/minio server /data
```

### mc(Minio Client)

Minio serverのセットアップ用CLIツール

```
$ docker run -it --entrypoint=/bin/sh minio/mc
```

### Webhook
  - [MinIO | Learn how to use MinIO Bucket Notifications](https://docs.min.io/docs/minio-bucket-notification-guide.html)
  - [minio/thumbnailer: A thumbnail generator example using Minio's listenBucketNotification API](https://github.com/minio/thumbnailer)


### その他SDK
  - [MinIO | AWS CLI with MinIO - Cookbook/Recipe](https://docs.min.io/docs/aws-cli-with-minio)
    - インストールとConfiguration
  - [MinIO | How to use AWS SDK for JavaScript with MinIO Server - Cookbook/Recipe](https://docs.min.io/docs/how-to-use-aws-sdk-for-javascript-with-minio-server.html)
    - AWS SDKでminioを接続して操作可能
  - [MinIO | JavaScript Client API Reference](https://docs.min.io/docs/javascript-client-api-reference.html)
    - minio serverとaws s3ともに使用できる（実行時の引数とかでわけれるかもね）
  - [MinIO | How to use AWS SDK for Python with MinIO Server - Cookbook/Recipe](https://docs.min.io/docs/how-to-use-aws-sdk-for-python-with-minio-server.html)
    - python用のAWS sdkであるboto3を用いてもminioを操作可能

## 参考リンク
### minio server
  - [Create default buckets via environment variables in docker · Issue #4769 · minio/minio](https://github.com/minio/minio/issues/4769)
  - [boto3でMinioのオブジェクトストレージにアクセスする(docker-compose)](https://qiita.com/th_/items/cf669949fe18f2eec5ab)
  - [LaravelからS3互換のMinIOを使えるように、docker-compose環境を整える](https://www.seeds-std.co.jp/blog/creators/2019-11-28-003000/)

### minio client
  - [MinIO | The complete guide to the MinIO client](https://docs.min.io/docs/minio-client-complete-guide)
  - [MinIO Server Config Guid](https://docs.min.io/docs/minio-server-configuration-guide.html)

### その他
  - [MinIO | Deploy MinIO on Docker Compose](https://docs.min.io/docs/deploy-minio-on-docker-compose.html)
  - [Synology NASにMinio on DockerをインストールしてS3互換サーバーにする](https://blog.ik.am/entries/441)
  - [Dockerネットワーク内のminioで署名付きURLを使う時のTIPS](https://n-s.tokyo/2019/04/minio-tips/)