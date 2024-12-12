FROM redis:6.2.6
LABEL authors="Hao <kyrieeeee2@gmail.com>"
COPY rediscluster.conf /etc/redis/rediscluster.conf
ENTRYPOINT redis-server /etc/redis/rediscluster.conf