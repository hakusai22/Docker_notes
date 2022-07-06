FROM minio/minio

LABEL maintainer="hakusai <hakusai22@qq.com>"

# 指定一个容器启动时要运行的命令，往往设置容器启动后的第一个命令
ENTRYPOINT ["minio", "server", "--console-address", ":9001", "/export"]
