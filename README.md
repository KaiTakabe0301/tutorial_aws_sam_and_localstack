# Tutorial AWS SAM and LocalStack
## 1. 初めに
このリポジトリは、[こちらの記事](https://zenn.dev/tkb/articles/75f2b8bdd6a106)で紹介している内容の完成物です。
AWS SAM + LocalStack + aws-sam-cli-local を利用してLocalStackとAWSの両方に```sam init``` で作成したプロジェクトを簡単にデプロイする方法を解説しています。

## 2. 実行環境
以下の環境でプロジェクトを構築しました。
* Docker Desktop 4.16.2
* SAM CLI, version 1.79.0
* Local stack community 1.4.0
* pipenv version 2021.11.23

## 3. 環境構築
以下の手順に沿って、環境を再現して下さい。

pythonの環境を再現
```bash
$ pipenv install
```

サンプルプロジェクトをビルド
```bash
$ sam build
```

LocalStackを起動
```bash
$ docker compose up -d
```

LocalStackにデプロイ
```
$ pipenv shell
$ samlocal deploy
```
