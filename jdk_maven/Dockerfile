# 使用Alpine作为基础镜像
FROM alpine:latest

# 更换镜像源为国内的镜像源
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories

# 更新包列表
RUN apk update

# 安装OpenJDK 17
RUN apk add --no-cache openjdk17

# 安装Git
RUN apk add --no-cache git

# 安装Maven
RUN apk add --no-cache maven


# 安装Neovim
# RUN apk add neovim

# 安装curl
# RUN  apk add curl

# 安装bash
# RUN apk add bash

# 设置工作目录
WORKDIR /app

# 将项目文件复制到容器中
COPY . /app

# 运行命令以保持容器不停止
CMD ["tail", "-f", "/dev/null"]
