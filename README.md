# laravel-vue-graphql

## Description

「実践！Laravel+Vue.jsではじめるGraphQL入門」本を参考にしてます。

## Usage

### Git settings(Windows Only...😇)

```
$ git config --global core.autocrlf false
```

### Git clone

```
$ git clone git@github.com:ucan-lab/laravel-vue-with-graphql-for-beginner
$ cd laravel-vue-with-graphql-for-beginner
```

### Docker compose build & up

```
$ docker-compose build
$ docker-compose up -d
```

### Composer Install

```
$ docker-compose exec app composer install
```

http://127.0.0.1:4000

### Running Migrations

```
$ docker-compose exec app php artisan migrate
```

## As necessary

### Login shell of the app container

```
$ docker-compose exec app ash -l
```

[alias settings](docker/php/aliases.sh) is enabled by `-l` option.

### MySQL connection

```
$ docker-compose exec db bash
$ mysql -u${MYSQL_USER} -p${MYSQL_PASSWORD} ${MYSQL_DATABASE}
```

### Node(npm, yarn)

```
$ docker-compose run node ash
$ npm install # OR yarn install
$ npm run dev # OR yarn run dev
```

### Redis for Laravel

```
$ docker-compose exec app ash
$ composer require predis/predis
$ sed -i -e 's/CACHE_DRIVER=.*/CACHE_DRIVER=redis/' .env
$ sed -i -e 's/SESSION_DRIVER=.*/SESSION_DRIVER=redis/' .env
```

### Redis cli

```
$ docker-compose exec redis ash
$ redis-cli
```
