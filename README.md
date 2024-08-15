### Laravel Docker 

起動コマンド
```
docker compose up -d
```

#### 初期設定

.env コピー
```
cp .env.example .env
```

composer install & APP_KEY 生成
```
// Dockerコンテナに入る
docker compose exec app bash

// Dockerコンテナ内で
composer install
php artisan key:generate
```

`http://localhost:8080/` にアクセスするとLaravelのトップ画面が見れます！

※Windowsユーザーはファイルの書き込み権限の問題でエラー画面が出るかもしれません。

適宜　`chown -R {user名}:{group名}` や `chmod -R 777` などのコマンドを使用して権限を変更してください。
