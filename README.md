# redis-cluster-playground

Run Redis in a docker container.

Replace `<path-to-repo>` to mount config & data directory in the Redis container.
```
docker run --name=redis -d --rm -p 6379:6379 -v <path-to-repo>/redis-cluster-playground/data:/redis/data -v <path-to-repo>/redis-cluster-playground/config:/redis/config redis
```

Example:
```
docker run --name=redis -d --rm -p 6379:6379 -v /home/capeta/workspace/redis-cluster-playground/data:/redis/data -v /home/capeta/workspace/redis-cluster-playground/config:/redis/config redis
```

Connect to redis container using bash
```
docker exec -it redis bash
```

Create Directory for storing pid files
```
mkdir -p /var/run/redis
```

Run Redis Processess
```
redis-server /redis/config/7000/redis.conf
redis-server /redis/config/7001/redis.conf
redis-server /redis/config/7002/redis.conf
redis-server /redis/config/7003/redis.conf
redis-server /redis/config/7004/redis.conf
redis-server /redis/config/7005/redis.conf
redis-server /redis/config/7006/redis.conf
redis-server /redis/config/7007/redis.conf
redis-server /redis/config/7008/redis.conf
```