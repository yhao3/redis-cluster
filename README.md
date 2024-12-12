# How to create local redis cluster

## Configure Redis Cluster

```bash
cp redis/rediscluster.conf.example redis/rediscluster.conf
```

Then edit `redis/rediscluster.conf` file:

```conf
# ip
bind 0.0.0.0
# 啟用 cluster
cluster-enabled yes
# 指定 cluster config 檔案
cluster-config-file nodes.conf
# 指定 node 無法連線時間
cluster-node-timeout 5000
#設置主服務的連接密碼
masterauth pass.123
#設置從服務的連接密碼
requirepass pass.123
```

## Build and Run

```bash
ip=xxx.xx.xx.xxx docker-compose up -d --build
```

> ![NOTE]
>
> Please replace `xxx.xx.xx.xxx` with your local ip address.

## Connect to Redis Cluster via [Redis Insight](https://redis.io/insight/)

Open your browser and visit `http://localhost:5540` to connect to Redis Cluster.
