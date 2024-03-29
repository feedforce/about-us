## 基本情報

https://dfplus.io

## プロダクト

### プロダクトの説明

dfplus.io は、マーケター向けのデータフィード管理ツール（SaaS）です。

Googleショッピング広告、Criteo、Facebookダイナミック広告など、近年ますます重要度が高まっている「商品データフィードを利用する各種広告」を効率的に管理する機能や、施策成果を高めるための最適化機能を直感的なUIで提供しており、多くの広告代理店様、事業会社様から支持されています。

主な機能として、

* 顧客が保有する商品データ（オンラインストアの商品、求人票データ、不動産物件データなど）の取込
* 柔軟で強力なデータ変換ルール
* 設定内容をわかりやすく確認できる広告クリエイティブプレビュー
* 複数サイト、複数データフィードの統合管理機能
* 広告媒体仕様に合わせてデータフィードの値を補正する自動最適化機能（[参考記事](https://dfplus.io/news/update-auto-optimization-20181227)）
* 作成されたデータフィードの仕様適合度を評価するスコアリング機能（[参考記事](https://dfplus.io/news/new-feature-datafeed-score)）
* 広告タイトルの自動改善機能（[参考記事](https://dfplus.io/news/new-feature-auto-improvement-for-google-shopping-20190828)）



を備えており、これらを用いてEC、人材、不動産、旅行などの業界でデータフィード広告に関わるマーケターのお仕事をサポートします。

[開発体制](https://media.feedforce.jp/n/n2e855d168e62)の記事をnoteで公開中です。


## 利用技術・開発環境

### 自動化していること

- 開発環境構築
- Lint
- テスト
- デプロイ

### 継続的に実践していること

- ChatOps
- Infrastructure as Code
- スクラム
- ペアプロ/モブプロ
- 事業数値をチーム全体に共有
- 毎日チーム全体で状況共有
- 定期的に振り返り
- キャリアアップの評価制度

### 利用している主要技術（本番環境で利用しているもの）

`AWS`, `EC2`,  `EKS`,  `Lambda`, `Aurora`, `DynamoDB`, `Terraform`, `Kubernetes`, `Rails`,  `TypeScript`, `React`, `redux`, `Heroku`, `Pusher`

### それ以外の開発環境や管理画面等で利用しているもの

`CirceCI`, `Docker`, `Datadog`, `Mackerel`, `Bugsnag`, `Redash`, `Amazon Athena`

### タスク管理・チャットツール等

`GitHub`, `GitHub Project`, `Slack`, `Zoom`, `esa`, `Figma`, `Trello`, `Google Spreadsheet`, `Miro`

## チーム全体での開発の進め方

### 開発・計画のサイクル

詳しくはこちらも一緒に御覧ください。
[エンジニア採用を強化しているので優秀なマネージャーと開発体制をアピールするよ｜フィードフォースのnote](https://media.feedforce.jp/n/n2e855d168e62)

スクラムをベースにした開発を行っています。UX/UI の設計と開発を同一イテレーション内で行っていないのが特徴的で、UX/UI を先のイテレーション内でプランニングし、開発が後のイテレーションで実装しています。これによって、開発が長くなったとしてもバックログアイテムのストックを増やすことができたり、 UX/UI についての議論を深くするための時間を増やしています。

1 スプリントは 1 週間です。初日に、今スプリントで実施するタスクを宣言することで達成したいゴールを明確にします。そして、毎日朝会(デイリースクラム)を行い、ゴールが達成できそうか共有することで問題の早期発見ができるよう心がけています。
最終日にレトロスペクティブ (KPT) を実施して、 1 スプリント通しての学びやカイゼン点を次回のスプリントに活かせるようにしています。

どのような機能をどのようなUX/UIで提供するかを議論する「プランニング」には、すべてのエンジニアとUXデザイナー、およびプロダクトマネージャーが参加しています。情報の非対称性をなくし、開発スピードを上げることを意識しつつ、必ずドキュメントに残すようにしています。参加できなかったメンバーや後から見返す際に齟齬がないようにしています。

タスクの管理には Google Spreadsheet, Trello, GitHub Issue/PR と GitHub Project を利用しています。

### 開発とリリース

開発フローは GitHub Flow を基本としていますが、リリース(デプロイ)は計画に従って任意のタイミングで実施しています。

1. Pull Request ベースでの開発(単独、ペア、モブ)
1. CI (Lint、単体テスト、結合テスト、E2E テスト、ビジュアルテスト)
1. 開発者レビュー(ペア、モブの場合は省略もあり)
1. レビュー環境作成(Heroku Review App / Render Pull Request Previews)
1. プロダクトオーナーレビュー
1. リリース(ChatOps)

機能開発と並行してユーザーガイドやプレスリリース、ユーザーアナウンスなども準備が進められており、それらと協調するために任意のタイミングでリリースできる方式を採用しています。

## 技術面でのアピール・課題・考え方

### 全体

- バックエンド、フロントエンド、インフラ、デザイナーとそれぞれの分野に特化したメンバーが揃っています
- フルリモートによる開発を行っており、ミーティングには Zoom を利用しています
- どの職能でもなるべく 2 人以上で相互にレビューおよびモブレビューしながら開発しています 
- イテレーションごとにエンジニア同士で深い開発共有を行っています
- 強制ではありませんが、ペアプロ・モブプロによる開発を推奨しています
- レビューや CI、技術的負債返済の文化がしっかりあります
- 属人化しないよう気をつけつつ、得意なことは各自でどんどんリードしてもらう雰囲気です
- 監視・通知は Slack に集約しています
- 週一でそれぞれの職能別のミーティングを行い情報共有や次週以降のタスク決めを行ってます

### バックエンド

- 主に 3 人で開発しています
- デプロイやオペレーション作業などの ChatOps にも積極的に取り組んでいます
- Docker を利用した開発環境で開発しています
- 主な技術スタックは [Ruby](https://www.ruby-lang.org/en/), [Ruby on Rails](https://rubyonrails.org/), [PostgreSQL](https://www.postgresql.org/), [Docker](https://www.docker.com/) です

### フロントエンド

- 主に 2 人で開発しています
- 日々の開発はペア/モブプロが中心です
- 単体テスト、E2E テスト、ビジュアル回帰テスト、型チェック、Lint、Bundle Analyzer を導入しており、安心して Pull Request をマージできる CI 構築に努めています
- 主な技術スタックは [TypeScript](https://www.typescriptlang.org/), [React](https://reactjs.org/), [Redux](https://redux.js.org/) です

### インフラ

- 専任は 1 人ですがバックエンドチームもインフラに理解があるため積極的に相談や協力しています
- より安定的なサービス稼働を目指し、インフラ構成の見直しや運用コストの削減、属人性の排除を重視しています
- 現在は EKS/Kubernetes を利用したサーバ環境のコンテナ化を進めています
- 主な技術スタックは [Kubernetes](https://github.com/kubernetes/kubernetes), [AWS](https://aws.amazon.com/), [Terraform](https://www.terraform.io/), [Chef](https://www.chef.io/), [Datadog](https://www.datadoghq.com/) です

### デザイナー

- 今は 1 人のデザイナーがアサインされています
- ステークホルダーの課題や解決策を素早く視覚化してチームに共有し、議論を進める「旗振り役」的な動き方が多いです
- 実際の開発に関してはたまにコーディングに参加したり実装レビューをしています
- 主な使用ツールは [Figma](https://www.figma.com/), [Sketch](https://www.sketch.com/), [Miro](http://miro.com/), [GitHub](https://github.com/), [Slack](http://slack.com/)です

### 課題

- 大量のバッチ処理を高速・安定・安価に実行できる基盤の実現
- メンテナンスなどに伴うサービス停止時間を極小化したシステムの実現
- 統計・機械学習的なアプローチでの「使いやすさ」「成果」向上

## 開発チームからのメッセージ

- メンバーの UX の理解度が高く、常にユーザーストーリーを意識して開発に取り組んでいます
- 職域またいで興味を持って意見出しができ、落とし所を探れるメンバーが揃っているチームです
- 課題や問題をチームのこととして捉えてチームでどう解決するのかを考えられるチームです
- 風通しの良いフラットで働きやすいチームです
- 不安に思ったことをすぐに共有できる場が用意されています
- 真面目な話をする時と、雑談をする時の切り替えがしっかりしています
