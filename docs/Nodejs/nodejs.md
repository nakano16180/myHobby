## 環境構築
nvmをインストール

```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash 
```

最新版のnodejsをインストール

```
$ nvm install --lts --latest-npm  
$ nvm alias default lts/* 
```

### direnv + nvm
複数プロジェクトでnodejsを使っていて、それぞれバージョンが違うことがあると切り替えがめんどくさくなる。  
そういうときにはdirenvが便利。

まず、goをインストール
```
$ sudo add-apt-repository ppa:longsleep/golang-backports  
$ sudo apt update  
$ sudo apt install golang-go  
$ go version  
```

次に、direnvをインストール

```
$ git clone https://github.com/direnv/direnv  
$ cd direnv/  
$ sudo make install  
```

その後、bashrcに以下を追記

```
export EDITOR=gedit  
eval "$(direnv hook bash)"  
```

### 使い方
プロジェクトのルートディレクトリで以下のコマンドを打つと .envrcファイルが作成される。  
これにより、このディレクトリに移動すると自動で .envrcファイルが読み込まれる。

```
$ direnv edit .
```

nodeのバージョン切り替えを行うためには .nvmrcファイルを作成し、使用したいnodeのバージョンを記述する。

あとは先ほどの .envrcファイルに以下を追記

```
nvmrc=~/.nvm/nvm.sh  
source $nvmrc  
nvm use  
```

これで完了

## json
  - [Node.jsでJSONを読み込んで加工して書き出す](https://qiita.com/usayuki/items/130c9cab7766d2997a7b)
  - [JavaScript オブジェクトの深くネストされているプロパティに安全にアクセスする getProperty](https://qiita.com/standard-software/items/bb044217d0a4b394b8e2)
  - [JavaScript オブジェクトの深くネストされているプロパティに値をセットする setProperty](https://qiita.com/standard-software/items/621a666b3d86e041b6a7)
  - [Node.jsで、pathを持っているファイル名配列を Tree構造のjsonに変換する方法](https://kokensha.xyz/javascript/turn-flat-path-array-to-json-tree-with-node-js/)

## ファイル操作
  - [File APIを使ってローカルのファイルを読み込んでみる](https://www.tam-tam.co.jp/tipsnote/javascript/post11736.html)
