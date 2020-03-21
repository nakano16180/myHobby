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
