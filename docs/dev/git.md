# git

## スクラムとgit

### Milestones
- スプリントバックログに利用
- 必ず期限を設定すること

### issues
- スプリントのタスク管理に利用

## 開発の流れ

### 1度だけする作業
1. 代表者のリポジトリをforkする
1. <自分の名前>/<リポジトリ名>になっていることを確認したら、developmentブランチをローカルにcloneする
1. upstreamという名前で代表者のリポジトリを登録する

### 開発の度に繰り返す作業
1. issueとMilestoneを確認する
1. developmentブランチから、dev_<作業内容>ブランチを作成する
1. キリの良いタイミングでaddとcommitを行う。<コメント> <#番号>でissueと関連付けを行う

### 開発が完了したら
1. developmentブランチに移動して、dev_<作業内容>をmergeする
1. dev_<作業内容>ブランチを削除する
1. developmentブランチをpushする
1. development -> master に <作業内容> -> masterというコメントでpull requestする
1. <自分の名前>/master -> <代表者の名前>/developmentにpull requestsする
1. 代表者のリポジトリに変更があればupstreamからpullする

### ただしコラボレーターの場合は
1. developmentブランチからdev_<名前>ブランチを作成する
1. dev_<名前>ブランチから更にdev_<作業内容>ブランチを作成する
1. 開発が完了したらdev_<名前>ブランチに移動してmerge->push


## ブランチ名
- 代表者/master: 本番リリース
- 代表者/development: 開発用
- 代表者/dev_<名前>: コラボレーター開発用ブランチ
- 代表者/dev_<作業内容>: 作業用

- コントリビューター/master: pull request用
- コントリビューター/development: 開発用
- コントリビューター/dev_<作業内容>: 作業用

### 作業内容一覧
- bug: バグ修正
- doc: 設計などドキュメント
- feature: 新機能