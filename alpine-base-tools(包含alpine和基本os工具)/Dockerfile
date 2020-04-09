FROM alpine:latest
# alpine 的相关操作见 https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management
MAINTAINER WeiguoLiu <liuwg-a@glodon.com>
USER root

# 切换到配置文件目录
WORKDIR /etc/apk
# 将官方仓库地址替换为阿里云的镜像地址
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' repositories

WORKDIR /root
# 更新本地索引
RUN apk update
# 1. 安装curl
RUN apk fetch curl
RUN apk add curl

# 让容器保持运行，保证不会退出，对应于centOS中的 /usr/sbin/init 命令，（如果要让空系统一直运行该命令必须加）
CMD init