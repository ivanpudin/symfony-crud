# Getting started

This app already includes [symfony-mamp](https://github.com/kalwar/Symfony-MAMP)

perform commands step by step

clone this repository

```
git clone
cd symfony-crud
cp .env.example .env && cp web/.env.example web/.env
docker-compose up --build
```

after container is created and running, get the id of Apache container

you can see it directly in docker, or using this command

```
docker ps
```

after you copied the id, perform this command

```
docker exec -it CONTAINER_ID /bin/sh
```

when you are in the container

```
cd web
php bin/console doctrine:database:create
php bin/console make:migration
php bin/console doctrine:migrations:migrate
```

choose 'yes', when asked

after that, you are done

app can be accessed at localhost:8007

database can be accessed at localhost:9082
