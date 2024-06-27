# Laravel Docker 環境

このリポジトリはLaravelアプリケーションのDocker環境を提供します。

## 初期設定

以下の手順に従って環境をセットアップしてください。

1. リポジトリをクローンする

   ```bash
   git clone https://github.com/Remin18/laravel-docker.git
   cd laravel-docker
   ```

1. Dockerコンテナを起動する

   ```bash
   docker-compose up -d
   ```

1. PHPコンテナに入る

   ```bash
   docker-compose exec php bash
   ```

1. .envファイルを作成

   ```bash
   cp .env.example .env
   ```

1. ファイルの所有者と権限を設定する

   ```bash
   chown -R www-data:www-data /var/www
   chmod -R 755 /var/www/storage
   ```

1. composerをインストール

   ```bash
   composer install
   ```

1. プロジェクトの依存関係をインストール

   ```bash
   npm install
   ```

1. APPキーを作成

   ```bash
   php artisan key:generate
   ```

1. データベースマイグレーションを実行する

   ```bash
   php artisan migrate
   ```

1. フロントエンドを起動

   ```bash
   npm run dev
   ```

## 注意事項

- 環境変数の設定が必要な場合は、`.env`ファイルを適切に設定してください。
- 追加のパッケージをインストールする場合は、`composer install`を実行してください。
