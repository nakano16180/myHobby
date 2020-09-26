## 環境構築

### Pipenv

- [公式リポジトリ](https://github.com/pypa/pipenv)

#### インストール

```
$ python3 -m pip install pipenv
```

bashrc に以下を追加

```
export PIPENV_VENV_IN_PROJECT=true
```

#### 参考リンク

  - [Python で、Pipenv を使う](https://narito.ninja/blog/detail/58/)
    - python 公式が正式に推薦しているツールらしい
  - [Pipenv ことはじめ](https://qiita.com/shinshin86/items/e11c1124e3e2e74556b8)
  - [複数人で使う python 製ツールの実行環境構築に pipenv を使ってみたら、とても便利だった](https://kapiecii.hatenablog.com/entry/2019/01/26/220000)
  - [【小ネタ】Pipfile にスクリプトショートカットを作成する](https://dev.classmethod.jp/articles/pipfile-scripts-shortcuts/)
  - [Pipenv の進んだ使い方](https://pipenv-ja.readthedocs.io/ja/translate-ja/advanced.html)
  - [Pipenv と Docker を使った開発環境のベストプラクティス](https://qiita.com/kawasin73/items/3e58fc8a14af66ab7204)
    - Docker で固めてるから他との依存含め環境を隔離できる
  - [きたない requirements.txt から Pipenv への移行](https://www.kabuku.co.jp/developers/python-pipenv-graph)
    - 今まで virtualenv と requirements.txt 使ってたのを Pipenv に移行するときの参考になりそう

### 良さげなページのリンク

  - [pip でインストールしたパッケージの場所を調べる](https://qiita.com/t-fuku/items/83c721ed7107ffe5d8ff)
  - [【Ubuntu】pip install –upgrade pip コマンドを実行すると、その後、ImportError: cannot import name main というエラーが発生する場合の対応方法](https://laboradian.com/cannot-import-name-main-when-upgrading-pip/)
  - [pip を直で使うのは非推奨っぽい？](https://qiita.com/taro-hida/items/16006f3622551e231a2e)

  - [Awesome Python on Qiita](https://qiita.com/hatai/items/34c91d4ee0b54bd7cb8b)
    - [document oriented database](https://github.com/msiemens/tinydb)
    - [postgres cli](https://github.com/dbcli/pgcli)
  - [invoke](https://github.com/pyinvoke/invoke)
    - cli ツール的なやつかな？
