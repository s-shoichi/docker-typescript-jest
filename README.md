# DockerでTypescript+Jest環境

## 0.前提
- Dockerのインストール
[Windows版はこちら](https://docs.docker.com/desktop/install/windows-install/)
[Mac版はこちら](https://docs.docker.com/desktop/install/mac-install/) ※ M1/M2のMacの場合は、「Apple silicon」を選択
- リポジトリのクローン

## 1. Dockerの立ち上げ
```
$ docker-compose up -d
$ docker-compose exec api-sample npm install  <- 初回のみ
```

## 2. テスト実行
```
$ docker-compose exec api-sample npm run test
```

## 3. DockerComposeコマンド
`Dockerコンテナの起動`
```
$ docker-compose up -d
`[-d]オプションをつけることでbackgroundで実行する。`
```

`Dockerコンテナのステータス確認`
```
$ docker-compose ps
```

`Dockerコンテナの停止`
```
$ docker-compose stop
```

`Dockerコンテナ内に入る`
```
$ docker-compose exec api-sample sh
```