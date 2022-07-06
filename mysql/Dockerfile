# 在执行 docker build 时，可以通过 --build-arg <参数名>=<值> 来为声明的变量赋值
# ARG 指令有生效范围, 如果在 FROM 指令之前指定，那么只能用于 FROM 指令中
# 要想在 FROM 之后使用，必须再次指定
ARG MYSQL_VERSION
FROM mysql:${MYSQL_VERSION}

LABEL maintainer="hakusai <hakusai22@qq.com>"

#####################################
# Set Timezone
#####################################
# ARG
# 作用：定义创建镜像过程中使用的变量
# ARG 和 ENV 的区别
#   1. ARG 定义的变量只会存在于镜像构建过程，启动容器后并不保留这些变量
#   2. ENV 定义的变量在启动容器后仍然保留
ARG TZ=UTC
ENV TZ ${TZ}
#运行linux命令
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone && chown -R mysql:root /var/lib/mysql/

# 将上下文目录中指定的文件复制带镜像的指定目录中去
COPY my.cnf /etc/mysql/conf.d/my.cnf

#运行linux命令
RUN chmod 0444 /etc/mysql/conf.d/my.cnf

# 启动的容器执行的命令，Dockerfile中只能有一条CMD指令，多个就最后一条生效
CMD ["mysqld"]
#对外暴露端口
EXPOSE 3306
