## slack拡張
### command
  - [Slack Appに挑戦(1) - WebhookとSlash Commandまで](https://qiita.com/kanaxx/items/a12a523ca3143b5822b8)
    - slash commandでslackを拡張（slash commandで外部にリクエストを投げ、Incomming Webhookでレスポンスを受け取るもよう）
    - Webhooksを受け取るサーバーをLalavelで構築し、Herokuにデプロイ（Masoniteで代用できるかな）
  - [Slackのslash command + Googleスプレッドシート + GASで貸出帳を作った](https://note.com/yuickomori/n/nb0ecbff77056)
  - [slackで「投稿ルールが守られない問題」を自作のスラッシュコマンドで解決する(設定編)](https://qiita.com/marogoma/items/e3003564c1b8b7b09e29)

### Bot
  - [[Slack]Botkitをherokuの無料プランで動かす方法](https://qiita.com/biga816/items/148a1156cd8b1a964b91)
    - BotkitというのをつかってBotをつくるところからHerokuにデプロイまで
  - [HubotをHerokuでSlackに繋げるまで](https://qiita.com/chibi929/items/79161111dee411000411)
  - [研究室のHPをサーバレス、SPA、GraphQL、ChatOpsで作った](https://qiita.com/asmsuechan/items/17f168f151346ac5cf65)
    - BotでWebページ管理
    - コマンドにいろいろオプションつくこと考えるとSlash commandよりボットのほうがいいのかも

#### Bolt
  - [Bolt 入門ガイド](https://slack.dev/bolt-js/ja-jp/tutorial/getting-started)
  - [Hubot のアプリを Bolt に移行する方法](https://slack.dev/bolt-js/ja-jp/tutorial/hubot-migration)
  - [Hello World, Bolt! ⚡️ Bolt フレームワークを使って Slack Bot を作ろう](https://qiita.com/girlie_mac/items/93538f9a69eb4015f951)
    - Glitchを使ったチュートリアル
  - [Slack の Bolt フレームワークのチュートリアルを Heroku 上で実行する](https://qiita.com/silverskyvicto/items/00102f988c10c267cf55)
    - Herokuで行うチュートリアル
    - これやったあとにBlockitなどを使ってさらに拡張するとスムーズに勉強を進められる

### UI 拡張
  - [Block Kit](https://api.slack.com/block-kit)
  - [Block Kit を使ってより情報的なレストラン検索コマンドを作ろう](https://api.slack.com/lang/ja-jp/slash-block-kit)
  - [Block KitでリッチなSlackアプリを作る -乗換経路案内での実例-](https://qiita.com/navitime_tech/items/85de33072486e7d323a5)
  - [SlackのBlock Kitを試す](https://www.dkrk-blog.net/slack/block_kit)
  - [Block Kit Builder を使ってインタラクティブな Slack アプリをプロトタイピングしよう](https://qiita.com/seratch/items/628751be65de9eb23a80)

### その他
  - [App interaction patterns](https://github.com/slackapi/app-interaction-patterns)
  - [SlackのIncoming WebhookアプリをGoを使ってメッセージ送信](https://ssabcire.hatenablog.com/entry/2019/12/13/143606)