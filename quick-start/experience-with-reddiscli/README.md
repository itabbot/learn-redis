# 使用 Redis 命令行界面体验最简单的 Redis 操作

```sh
# 进入 Redis 的 Docker 容器中并使用 Redis 命令行工具连接 Redis
$ sudo docker exec -it redis redis-cli
127.0.0.1:6379>

# 选择第1个数据库
127.0.0.1:6379> select 1
OK

# 设置一个键值对
127.0.0.1:6379[1]> set key1 val1
OK

# 通过键名获取值
127.0.0.1:6379[1]> get key1
"val1"

# 查看所有键名
127.0.0.1:6379[1]> keys *
1) "key1"

# 删除键值对
127.0.0.1:6379[1]> del key1
(integer) 1
127.0.0.1:6379[1]> keys *
(empty array)
```
