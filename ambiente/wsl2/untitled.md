# Docker na WLS 2

First, you have to [install Docker in Windows Host ](https://docs.docker.com/docker-for-windows/install-windows-home/)

Add this to you wsl bash profile:

```text
export DOCKER_HOST=unix:///var/run/docker.sock
```

## Create docker image to PostgreSQL

```text
docker run -d --name pg -v ~/temp/postgresql/data:/var/lib/postgresql/data -p 5432:5432 -e POSTGRES_HOST_AUTH_METHOD=trust postgres

docker stop pg
docker start pg
```

## Create docker image to Redis

```text
docker run -v ~/temp/conf/redis.conf:/usr/local/etc/redis/redis.conf -p 6379:6379 --name redis redis

docker stop redis
docker start redis
```

## Create docker image to PostgreSQL

```text
docker run -d --name pg -v ~/temp/postgresql/data:/var/lib/postgresql/data -p 5432:5432 -e POSTGRES_HOST_AUTH_METHOD=trust postgres

docker stop pg
docker start pg
```

