Masonite tutorials

```
$ mkdir masonite_tutorial
$ cd masonite_tutorial/
$ virtualenv -p python3.6 .venv
$ source .venv/bin/activate

$ pip3 install masonite
$ craft new
$ craft serve

```

## [公式チュートリアル](https://docs.masoniteproject.com/creating-a-blog)

ブログを作った。  
ルーティングは以下のようになっている。

  - http://localhost:8000
  - http://localhost:8000/register
  - http://localhost:8000/login
  - http://localhost:8000/home
    - blogへのリンクほしい
  - http://localhost:8000/blog
    - 「Post!」を押すと/blog/createにpostされ、/blog/postにリダイレクト
  - http://localhost:8000/blog/crate
  - http://localhost:8000/posts
    - 投稿一覧画面
  - http://localhost:8000/post/1
    - 投稿の詳細ページ
    - 投稿一覧からリンクしたい
  - http://localhost:8000/post/1/update
    - 投稿をupdate or delete
    - 投稿の詳細ページからリンクしたい
