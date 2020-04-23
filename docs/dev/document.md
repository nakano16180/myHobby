## ドキュメント管理ツール
  - MkDocs
    - [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)
  - [VuePress/Netlify](https://qiita.com/ozaki25/items/a1988b01f83f6616b7f9)
  - [HuckMDとGithub連携](https://1o0.jp/blog/post/201908/hugo-by-huckmd-github-netlify/)

### MkDocs
  - [【年末大掃除】.mdをCI/CDで整理する](https://tech-blog.optim.co.jp/entry/2019/12/25/173000)
    - GitLabでドキュメント作成を自動化
    - 既存のプロジェクトのドキュメントサイトをMkdocsで作ってGitLab Pagesで公開
  - [git-revision-date-localizedプラグイン](https://roy-n-roy.github.io/mkdocs/gitRevisionDate/)
    - 更新日時を表示できる
  - [GitHub Actions による GitHub Pages への自動デプロイ](https://qiita.com/peaceiris/items/d401f2e5724fdcb0759d)
    - プッシュしたら自動でデプロイ
  - [GitHub Actionsを利用したMkDocsの自動デプロイ](https://roy-n-roy.github.io/mkdocs/githubActions/)
    - プッシュしたら自動でデプロイ(上のやつよりもう少し詳しい設定ある)

#### サンプル集
  - MkDocs
    - [ドキュメントページ](https://www.mkdocs.org/)
    - [yamlファイル](https://github.com/mkdocs/mkdocs/blob/master/mkdocs.yml)
  - OpenFaaS
    - [ドキュメントページ](https://docs.openfaas.com/)
    - [yamlファイル](https://github.com/openfaas/docs/blob/master/mkdocs.yml)
  - Keras Document
    - [ドキュメントページ](https://keras.io/ja/)
    - [yamlファイル](https://github.com/keras-team/keras-docs-ja/blob/master/mkdocs.yml)
  - pymdown extension
    - [ドキュメントページ](https://facelessuser.github.io/pymdown-extensions/)
    - [yamlファイル](https://github.com/facelessuser/pymdown-extensions/blob/master/mkdocs.yml)

### Github pages
  - プロジェクトごとにドキュメントページを生成してgithubにホスティングできる
  - リポジトリ名に _ を含むのはだめっぽい