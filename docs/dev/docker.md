## Docker
[公式ページ](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

### uninstall old version

```
$ sudo apt remove docker docker-engine docker.io containerd runc
```

### install Docker Engine
#### set up the repository

```
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

#### install docker engine - community

```
$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
```

### uninstall docker engine - community

```
$ sudo apt purge docker-ce
$ sudo rm -rf /var/lib/docker
```

## docker-compose
[公式ページ](https://docs.docker.com/compose/install/)
```
$ pip3 install docker-compose
```

## GPU Docker
  - [NVIDIA Docker って今どうなってるの？ (19.11版)](https://qiita.com/ksasaki/items/b20a785e1a0f610efa08)

## 参考資料
  - [Dockerコンテナのシェルの中に入る](https://qiita.com/__cooper/items/4740c24666299c366044)
  - [Dockert調査　~ログ編~](https://qiita.com/HommaHomma/items/f943fa3397bc3f386057)
  - [docker-compose logs](https://docs.docker.com/compose/reference/logs/)
  - [docker-compose コマンドまとめ](https://qiita.com/wasanx25/items/d47caf37b79e855af95f)
  - [docker-compose.ymlで.envファイルに定義した環境変数を使う](https://kitigai.hatenablog.com/entry/2019/05/08/003000)
  - [docker-compose コマンド](http://docs.docker.jp/compose/reference/docker-compose.html)
    - -f オプションで、カスタムのdocker-composeファイルを指定
  - [docker と docker-compose の初歩](https://qiita.com/hiyuzawa/items/81490020568417d85e86)
  - [Dockerfileとdocker-compose.ymlが何を書いてるか読み解こう](http://tech.innovation.co.jp/2018/01/26/read-docker-files.html)
  - [Dockerのログのクリア方法とローテーション設定について](https://note.com/funmylife/n/nc3210727e11f)