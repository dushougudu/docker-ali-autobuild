FROM alpine:latest
# alpine 的相关操作见 https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management
MAINTAINER WeiguoLiu <liuwg-a@glodon.com>
USER root

RUN apk update
RUN apk fetch openjdk8
RUN apk add openjdk8
# 修改时区为上海
RUN apk add tzdata
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN apk del tzdata