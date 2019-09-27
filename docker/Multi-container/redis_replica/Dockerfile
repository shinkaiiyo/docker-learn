FROM shinkaiiyo/redis
MAINTAINER shinkaiiyo <m18235896053@gmail.com>
ENV REFRESHER_AT 2019-09-27
ENTRYPOINT [ "redis-server","--logfile /var/log/redis/redis-replica.log","--slaveof redis_primary 6379" ]
