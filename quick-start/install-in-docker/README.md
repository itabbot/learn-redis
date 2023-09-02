# 使用 Docker 安装 Redis

1. 拉取 Redis 的最新版 Docker 镜像（[其他版本>>](https://hub.docker.com/_/redis/tags)）

```sh
$ sudo docker pull redis

Using default tag: latest
latest: Pulling from library/redis
52d2b7f179e3: Pull complete 
689bed60e397: Pull complete 
2f34c7846499: Pull complete 
723b2c9888ad: Pull complete 
16acd9ca1349: Pull complete 
29771da5b50b: Pull complete 
Digest: sha256:c45b9ac48fde5e7ffc59e785719165511b1327151c392c891c2f552a83446847
Status: Downloaded newer image for redis:latest
docker.io/library/redis:latest
```

2. 将镜像作为容器运行

```sh
$ sudo docker run --name redis -d redis
7317b12029d99d85d78fe5f31da0f8494b394a0540392b04eac9f3e6beef1ed0
```

3. 检查容器是否正在运行

```sh
$ sudo docker container ls

CONTAINER ID   IMAGE     COMMAND                   CREATED          STATUS          PORTS      NAMES
7317b12029d9   redis     "docker-entrypoint.s…"   43 seconds ago   Up 42 seconds   6379/tcp   redis
```

4. 进入容器中并使用 Redis 命令行工具连接 Redis

```sh
$ sudo docker exec -it redis redis-cli
127.0.0.1:6379> 
```
