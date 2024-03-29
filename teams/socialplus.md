## 基本情報

https://socialplus.jp

## プロダクト

### プロダクトの説明

ソーシャルPLUS は、2012年4月にリリースされた、エンドユーザーの会員登録や再ログインがかんたんになる「ソーシャルログイン」を一括で実装できる BtoBtoC の ID 連携サービスです。対応する認可プロバイダには LINE や Apple, Twitter, Facebook, Yahoo! JAPAN, Google などがあります。

その一方で、ソーシャルPLUS は企業のマーケターからも注目されるサービスでもあります。理由としては、

* 従来のようにマーケティングメールを一斉配信してもブロックされてしまう
* そもそもメールを開封してくれないユーザーが増えている
* 近年では 3rd Party Cookie の規制により Cookie ベースのトラッキングが難しくなってきた

という背景から「ソーシャルログインを起点にエンドユーザーと接点を持ち、コミュニケーションを取りたい」というニーズがあるためです。

ソーシャルPLUS は LINE のようなサービスと、企業の持つ顧客情報を ID 連携させ、顧客情報に基づいた最適なコミュニケーションの方法を提供し、エンドユーザーにとってより良い体験を提供するサービスを目指しています。これを実現するため、2016年からは LINE を通じたメッセージ配信などの機能にも注力しています。

2020年からは、EC プラットフォームとして注目されている Shopify 向けの[アプリ](https://socialplus.jp/shopify_app/)も提供しています。

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

### テストについて

テストコードは当たり前のように書かれており、高いカバレッジが維持されています。

### 技術的負債について

プロダクトの成長スピードを優先する時期もありますが、意識的に技術的負債の返済の期間も設けて対応しています。

### コードレビューについて

基本的には設計に踏み込んだコードレビューをしています。モブプロなどとの組み合わせでやっています。

### 利用している主要技術（本番環境で利用しているもの）

`AWS`, `Amazon EKS`, `Kubernetes`, `Rails5`, `Rails6`, `Terraform`, `TypeScript`, `React`, `Next.js`, `Preact`, `Redux`, `Heroku`, `Firebase`

### それ以外の開発環境や管理画面等で利用しているもの

`Scout APM`, `CirceCI`, `GitHub Actions`, `Docker`, `Datadog`, `Bugsnag`, `Redash`, `Storybook`, `LogRocket`, `Argo CD`

### タスク管理・チャットツール等

`GitHub`, `GitHub Project`, `Slack`, `Slack Huddles`, `esa`, `Zoom`, `Figma`, `Miro`

## チーム全体での開発の進め方

### イテレーションと計画

スクラムに則った開発を行っており 1 イテレーションを 2 週間として、イテレーション開始日に計画を行い、最終日にレビューと振り返り (KPT) を実施しています。また、毎日朝会 (デイリースクラム) を行い、前日の作業と今日の予定などを共有しています。

意識しているのはチームの同期と非同期で、イテレーション中は各々が非同期に自分のタスク集中できるよう、計画や朝会のタイミングで個々人とチーム全体の同期をとるようにしています。

タスクの管理には GitHub Issue/PR と GitHub Project を利用しています。

### 現在の課題と優先事項

システムとしては、多くの企業にソーシャルログイン機能を提供しているため、安定した稼働率が求められるサービスです。

一方で LINE や Shopify のように多くの企業が注目するサービスとの連携や、新しいログインプロバイダーの追加なども行っています。また、過去にリリースした機能でニーズが低く負債となっている機能を削除する対応も随時行っています。

以上のことから、安定したシステム稼働と新機能追加、技術的負債の返済をバランス良く計画的に行うことに努めています。

### 開発とリリース

GitHub Flow に基づいて開発を行っており、作成した Pull Request (PR) はチームメンバー間でレビューを行います。PR を作成すると、CircleCI 上で自動的にテストが実行されます。

デプロイ作業は、Slack を利用した ChatOps によって行います。staging 環境での動作確認とレビューを経て、本番環境へデプロイという流れになります。

## 技術面でのアピール・課題・考え方

### 全体

- Ruby on Rails を用いた開発経験の長いバックエンドエンジニアがリーダーです
- バックエンド・フロントエンド・インフラ、それぞれの分野に特化したエンジニアが揃っています
- フルリモートによる開発を行っており、ミーティングには Zoom を利用しています
- どの職能でもなるべく 2 人以上で相互にレビューをしながら開発しています
- イテレーションごとにエンジニア同士で深い開発共有を行っています
- 強制ではありませんが、ペアプロ・モブプロによる開発を推奨しています
- レビューや CI、技術的負債返済の文化がしっかりあります
- 属人化しないよう気をつけつつ、得意なことは各自でどんどんリードしてもらう雰囲気です
- 監視・通知は Slack に集約しています
- 週一で会社全体のエンジニア・デザイナーが集まって行う社内勉強会があります

### バックエンド

- 主に 5 人で開発しています
- 日々の開発はペアプロが中心です
- 開発環境は Docker 上に構築した Rails システムです
- CI 上で RSpec や RuboCop を実行し、テストカバレッジを計測しています。テストカバレッジはなるべく 100% に近い状態を目指しています
- 主な技術スタックは Ruby, Ruby on Rails, MySQL, Docker です

### フロントエンド

- 主に 3 人で開発しています
- タスクに応じて、ペアプロとソロプロを使い分けています
- 安全で保守性の高いコーディングを行っています
- Testing Library による UI テストや、Storybook + Storycap + reg-suit によるビジュアルリグレッションテストを強化中です
- 主な技術スタックは TypeScript, React, Next.js, Redux です

### インフラ

- 主に 3 人で開発しています
- より安定的なサービス稼働を目指し、インフラ構成の見直しや運用コストの削減、属人性の排除を重視しています
- 現在は Kubernetes を利用したサーバ環境のコンテナ化を進めています
- 主な技術スタックは Kubernetes (EKS), AWS, Terraform, Datadog, Argo CD です

### デザイナー

- 主に 2 人で開発しています
- チーム内外のメンバーと積極的に関わってデザインします
- ステークホルダーの課題や解決策を素早く視覚化してチームに共有します
- 会社全体のブランディング整備にも取り組んでいます
- 主な使用ツールは、Adobe XD, Figma, Miro です

### 課題

サービスの成長の伴って一人ひとりの守備範囲が大きくなってきました。
各自が自分の開発に集中できるよう、チームを分割して各チームの責任範囲を定め、自律的な組織を作っていきたいと考えています。
自律的な組織を作っていく上ではマネジメントやリードを担当できるエンジニア・デザイナーの存在が重要になってきます。

- チーム毎にビジネスサイドの要望から要件定義・設計・開発進行のマネジメントできるエンジニア・デザイナーを配置したい
- 専門分野毎にプロダクトの品質管理を担当できるテックリード・リードデザイナーを配置したい
- 将来的に上記のようなポジションを目指したいという方も増えて欲しい

## 開発チームからのメッセージ

ソーシャルPLUS は表立って目立つことは無いですが、エンドユーザーと企業をつなぐサービスとして多くのサイトに導入されているサービスです。

その裏側では、認証認可などの専門的な知識を駆使した設計や、LINE や Shopify といった様々なサービスと連携した新しい機能の実装、個人情報を外部に漏らさないようなセキュリティ面への配慮や、突発的に増えるトラフィックへの対応など、日々新しい挑戦を続けています。

一方で、開発メンバー各々のワーク・ライフ・バランスも大事にしており、個々人の残業時間への配慮や男性エンジニアの育休取得などにも積極的に取り組んでいます。

開発チームの風通しも良く、各々が感じた課題感をチーム全体で共有・解決できる風土を大切にしています。

これからもエンジニア・デザイナーにとってより良い開発環境を目指していきますので、是非一緒にさいこう！の環境でさいこう！のサービスを作っていきましょう！

![ダンスをしている動物達のイラスト \| かわいいフリー素材集 いらすとや](https://1.bp.blogspot.com/-t9m-a6qtpLs/UUFxmJCWzhI/AAAAAAAAOxY/XLHdtZSqvtw/s400/animal_dance.png)
