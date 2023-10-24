# スキルシート
## 基本情報
|  |  |
| --- | --- |
| 名前 | 川端健治 |
| 年齢 | 38 |
| 最寄り駅 | 都営大江戸線　光が丘駅 |
## 得意分野
- AWSを使用した環境構築/運用
- IaCツールやCI/CDツールを用いての構築/デプロイの自動化
- 関連部署と適宜連携してその状況に応じた最適なプロジェクト進行
## スキルセット
- 基本的にすべて実業務で使用した技術だけを列挙しています。
### 言語
- いずれもWebフレームワークを用いたシステム実装はありませんが、関数やツールの作成等は可能です
  - Rust | TypeScript | Python | シェルスクリプト
### DB
- MySQL | PostgreSQL
### クラウド
- AWS
  - VPC | S3 | CloudFront | Lambda | ELB | EC2 | ECS | Fargate | Beanstalk | Route53 | IAM | RDS(MySQL|PostgreSQL) | ElastiCache(Redis) | SQS | SNS | CloudFormation | CloudWatch | Step Functions
- Azure
  -  Azure ActiveDirectory | Virtual Machines | App Service
### CI/CD
  -  GitHub | GitHub Actions | CircleCI | Azure Devops
### IaC
  -  AWS CDK | CloudFormation | terraform | Ansible | Packer
### monitoring
  -  CloudWatch | Datadog | mackerel | NewRelic | nagios | Zabbix
## 主な業務経歴
### エレベーターサイネージの広告配信サービスの構築、運用(2022年4月〜現在)
- アプリケーションの刷新に伴う新システムの構築
  - 別のプロジェクトで使用していたアプリケーションを流用して使用していたが、当プロジェクト専用のアプリケーションの作成を行うにあたりインフラ基盤も新規に構築
    - AWS CDKテンプレート(TypeScript)でS3、RDS、ElastiCache、AppMesh、ECR、ECSのコード化
    - 負荷状況に応じたスケールアウト、スケールインの設定
    - 旧システムから新環境への移行
- モニタリング設定
  - システムの状態を可視化したダッシュボード、アラート通知(メトリクス異常値/エラーログ)の機構の作成
  - マネージドサービスのイベント通知
- メンテナンス/システム更新対応
  - RDSのバージョンアップ
    - Aurora MySQL(MySQL5.7互換)EOL対応、開発チームの機能要望のため
  - ElastiCacheのクラスターモード対応
    - クラスターモードがOFFの場合、プライマリーノードにリクエストが偏っておりプライマリーノードと異なるアベイラビリティゾーンのECSタスクからのレスポンスが悪かった
  - ECSのServiceConnect対応
    - AppMeshよりも管理コストが低減できる
- 各種トイルの見直し
  - CI／CD設定
    - Githubのアプリケーションリポジトリからdockerイメージのビルド、コンテナリポジトリへのpush、アプリケーションの更新を行うGithub Actionsのワークフローの作成
  - データベースのマイグレーションを行うGithub　Actionsのワークフロー作成
- 新機能検討
  - ビジネスメンバーと今後必要な機能を適宜検討
    - QRコードで効果計測、物件の属性に応じた最適化配信(ペット可の物件に〜、食洗機のある物件に〜)、広告の自動作成のような案のみのものも含め

### 自社開発/受託開発併用企業での業務(2021年7月〜2022年3月)
- オンラインイベント用のプラットフォーム環境構築
  - 既存環境を基にした新プラットフォームの構築
    - terraformのパラメーター修正、実行によるAzureの環境構築
- 省庁向けシステムのインフラ構築
  - 公募案件の提案資料、基本設計、インフラ構築
    - 要件定義書を基にした提案資料の作成、システム基盤の基本、詳細設計
  - 受注した案件のシステム構築

### 大手企業の系列企業における自社サービス開発業務(2020年3月〜2021年10月)
- 情報銀行アプリの運用/保守
  - 運用業務
    - チーム入れ替わりにより引き継ぎが十分に行われずブラックボックス化していた業務のキャッチアップ/フォロー
  - 定型業務の自動化
  - エラー/障害対応、AWSコスト削減
- 放送局と連携した情報銀行サービスの設計、構築
  - AWS基盤の構築、開発下請け会社との調整

###　教育系アプリのシステム構築、運用/保守(2019年4月〜2020年2月)
- terraformを使用しての自動構築
- CircleCIを使用してのデプロイ自動化

###　音楽系ECサイトの構築、運用/保守(2016年10月〜2019年3月)
- デプロイフローの整備
- Packerを使用して構築手順のテンプレート化
- サーバのOSアップデート
- ミドルウェアの導入、チューニング

