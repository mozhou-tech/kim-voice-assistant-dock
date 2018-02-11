# 定义一系列环境变量

FROM python:3.6-alpine3.7
LABEL author=tenstone
ENV PROJECT_DIR="kim-voice-assistant-server" PROJECT_GIT_PATH="https://github.com/tenstone/kim-voice-assistant-server.git"

    # 安装git
RUN apk --no-cache add git gcc g++ make libffi-dev openssl-dev

# 进入工作目录
WORKDIR /usr/src/app

# 获取代码
RUN git clone $PROJECT_GIT_PATH

# 处理项目文件
WORKDIR /usr/src/app/$PROJECT_DIR
RUN cp setting-example.yaml setting.yaml && \
    git pull && \
    # 安装py package
    pip install --no-cache-dir -r requirements.txt

CMD [ "python", "run.py" ]