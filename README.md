# Laravel Training

## see
* http://laradock.io/
* https://readouble.com/laravel/5.6/ja/installation.html

## initial way
```bash
# Docker開発環境の用意
$ git clone https://github.com/Laradock/laradock.git
$ cd laradock 
$ cp env-example .env
$ docker-compose up -d nginx mysql phpmyadmin redis workspace

# Laravel projectの作成
$ docker exec -it laradock_workspace_1 bash
> composer create-project laravel/laravel app
> exit

# Laravel projectをdocker containerに認識させる
$ vim .env
APP_CODE_PATH_HOST=../ ⇒ APP_CODE_PATH_HOST=../app
```

ここまでで http://localhost/ にアクセスできるようになっている



