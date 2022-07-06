FROM redis:latest

LABEL maintainer="hakusai <hakusai22@qq.com>"

## For security settings uncomment, make the dir, copy conf, and also start with the conf, to use it
#RUN mkdir -p /usr/local/etc/redis
#COPY redis.conf /usr/local/etc/redis/redis.conf

# 使用数据卷挂在目录
VOLUME /data
# 暴露端口
EXPOSE 6379

CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]
#CMD ["redis-server"]
