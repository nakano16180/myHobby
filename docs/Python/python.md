## 環境構築
### virtualenv
  - [Python の実行環境を切り替えて使用する (virtualenv)](https://maku77.github.io/python/env/virtualenv.html)
  - [【Python】Virtualenvを使った仮想環境の構築](https://hibiki-press.tech/learn_prog/python/virtualenv/4545)

### Pipenv
  - [公式リポジトリ](https://github.com/pypa/pipenv)
#### インストール

```
$ python3 -m pip install pipenv
```
bashrcに以下を追加

```
export PIPENV_VENV_IN_PROJECT=true
```
#### 参考リンク
  - [pyenv、pyenv-virtualenv、venv、Anaconda、Pipenv。私はPipenvを使う。](https://qiita.com/KRiver1/items/c1788e616b77a9bad4dd)
    - よく聞く仮想環境のツールと比較されていて良い
  - [Pythonで、Pipenvを使う](https://narito.ninja/blog/detail/58/)
    - python公式が正式に推薦しているツールらしい
  - [複数人で使うpython製ツールの実行環境構築にpipenvを使ってみたら、とても便利だった](https://kapiecii.hatenablog.com/entry/2019/01/26/220000)
  - [【小ネタ】Pipfileにスクリプトショートカットを作成する](https://dev.classmethod.jp/articles/pipfile-scripts-shortcuts/)
  - [Pipenv と Docker を使った開発環境のベストプラクティス](https://qiita.com/kawasin73/items/3e58fc8a14af66ab7204)
    - Dockerで固めてるから他との依存含め環境を隔離できる
  - [きたない requirements.txt から Pipenv への移行](https://www.kabuku.co.jp/developers/python-pipenv-graph)
    - 今までvirtualenvとrequirements.txt使ってたのをPipenvに移行するときの参考になりそう
  - [Pipfile/Pipfile.lockの必要性 -requirements.txtを用いる手法と比較して-](https://qiita.com/miyashiiii/items/92e6f745a940c4df2ddd)
    - タイトル通り、Pipfileの良さがわかる（気がする）

## 良さげなページのリンク
  - [Awesome Python on Qiita](https://qiita.com/hatai/items/34c91d4ee0b54bd7cb8b)
    - [document oriented database](https://github.com/msiemens/tinydb)
    - [postgres cli](https://github.com/dbcli/pgcli)
  - [invoke](https://github.com/pyinvoke/invoke)
    - cliツール的なやつかな？
  - [Diagramsを使ってPythonでシステム構成図を描く](https://dev.classmethod.jp/articles/diagrams-introduction/)
  - [Python3 で JSON の読み書きをする方法（WebAPI にも対応） – サンプルコード付](https://www.craneto.co.jp/archives/1331/)