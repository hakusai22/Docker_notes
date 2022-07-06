FROM python:2.7

LABEL maintainer="hakusai"

# 设置环境变量
ENV PYTHONUNBUFFERED 1

ARG APP_CODE_PATH_CONTAINER=/hakusai_code

# 在根目录创建文件夹
RUN mkdir ${APP_CODE_PATH_CONTAINER}
# 设置工作目录
WORKDIR ${APP_CODE_PATH_CONTAINER}
# 复制requirements.txt
COPY requirements.txt ${APP_CODE_PATH_CONTAINER}
# 安装依赖, 清华源:https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip install -i https://pypi.doubanio.com/simple -r ${APP_CODE_PATH_CONTAINER}/requirements.txt

# 把本地文件拷贝到容器
# ADD . /code/

# 开放端口
# EXPOSE 8000