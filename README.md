# 環境構築方法

## 1. GitHubリポジトリURLを自身のPCにクローン
```zsh
git cline git@github.com:chika-bac/rails-docker.git

# クローンしたリポジトリに移動
cd rails-docker
```

## 2. 以下コマンドを実施してコンテナを起動
```zsh
docker-compose up
```

## 3. コンテナ内にDBを作成
ターミナルの別タブを開き、以下コマンドを実行
```zsh
docker compose exec web rails db:create
docker compose exec web rails db:migrate
```

## 4. ブラウザで動作確認
`http:localhost:3000`にアクセスし、表示確認をする
