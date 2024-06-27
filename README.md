# Laravel Docker 環境

このリポジトリはLaravelアプリケーションのDocker環境を提供します。

## 初期設定

以下の手順に従って環境をセットアップしてください。

1. リポジトリをクローンする

   ```bash
   git clone https://github.com/Remin18/laravel-docker.git
   cd laravel-docker
   ```

2. Dockerコンテナを起動する

   ```bash
   docker-compose up -d
   ```

3. PHPコンテナに入る

   ```bash
   docker-compose exec php bash
   ```

4. ファイルの所有者と権限を設定する

   ```bash
   chown -R www-data:www-data /var/www
   chmod -R 755 /var/www/storage
   ```

5. データベースマイグレーションを実行する

   ```bash
   php artisan migrate
   ```

## 注意事項

- 環境変数の設定が必要な場合は、`.env`ファイルを適切に設定してください。
- 追加のパッケージをインストールする場合は、`composer install`を実行してください。
