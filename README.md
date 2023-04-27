dbのパスワードがなぜか
`secret`
です
<br>
.env
を作ってね

# 開発環境のセットアップ

```
git clone --recursive git@github.com:posse-ap/teamdev-2023-posse2-team2C.git

```

※ サブモジュールがクローンされない場合
1. GitHubアカウントにログインします。
2. プロフィール画面の右上にあるアイコンをクリックし、「Settings」を選択します。
3. 「Developer settings」を選択し、「Personal access tokens」をクリックします。
4. 「Generate new token」をクリックして、新しいトークンを生成します。必要なスコープを設定して、トークンを生成します。
5. トークンをコピーして、clone時に求められるパスワード入力欄に貼り付けます。

```
docker-compose build --no-cache
docker-compose up -d
docker exec -it {teamdev-2023-posse2-team2c_appのコンテナID} bash
composer install
exit
cd api
cp .env.example .env
```

envを以下に変更する
```
APP_NAME=Laravel
APP_ENV=local
APP_KEY=base64:GTnvVFS7m53DDDrWbx185abB7xlKkzcCXywYz/ffdHo=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=phper
DB_PASSWORD=secret

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailpit
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_HOST=
PUSHER_PORT=443
PUSHER_SCHEME=https
PUSHER_APP_CLUSTER=mt1

VITE_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
VITE_PUSHER_HOST="${PUSHER_HOST}"
VITE_PUSHER_PORT="${PUSHER_PORT}"
VITE_PUSHER_SCHEME="${PUSHER_SCHEME}"
VITE_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"
```