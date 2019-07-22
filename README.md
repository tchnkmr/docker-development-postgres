# ローカル開発用Postgres

## 概要

ローカル開発で使用してPostgresサーバを立てたい場合に、Dockerで簡単にPostgresサーバを起動する方法です。
また、データをローカルのストレージに永続化します。

## 手順

1. Postgresの使用するDockerイメージの取得

　　[Postgresバージョン](https://hub.docker.com/_/postgres)

  　　`docker pull postgres:<version>`

2. docker-compose.ymlの編集

  サンプルのdocker-compose.ymlの編集

  |項目|内容|
  |:---|:--|
  |version|1.で取得したMySQLのバージョン|
  |local_storage|データを保存するローカルパス|
  |passwrod|ルートパスワード|

3. 起動

  `docker-compose up -d`

4. 停止

  `docker-compose stop`
