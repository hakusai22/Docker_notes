FROM mongo:latest

LABEL maintainer="hakusai <hakusai22@qq.com>"

#COPY mongo.conf /usr/local/etc/mongo/mongo.conf

# 作用：创建一个匿名数据卷挂载点
# 格式： VOLUME ["/data"]
# 详解：运行容器时可以从本地主机或其他容器挂载数据卷，一般用来存放数据库和需要保持的数据等
# 其实VOLUME指令只是起到了声明了容器中的目录作为匿名卷，但是并没有将匿名卷绑定到宿主机指定目录的功能。
# volume与-v指令一样，容器被删除以后映射在主机上的文件不会被删除。
VOLUME /data/db /data/configdb

CMD ["mongod"]

EXPOSE 27017

