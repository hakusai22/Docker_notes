FROM rabbitmq:alpine
# 维护者
LABEL maintainer="hakusai <hakusai22@qq.com>"
# 运行linux命令
RUN rabbitmq-plugins enable --offline rabbitmq_management
# 暴露端口
EXPOSE 4369 5671 5672 15671 15672 25672
