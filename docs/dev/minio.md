## Object storage for Local

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
