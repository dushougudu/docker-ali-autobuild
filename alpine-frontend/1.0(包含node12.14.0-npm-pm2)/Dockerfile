FROM alpine:latest
MAINTAINER WeiguoLiu <liuwg-a@glodon.com>
USER root

RUN apk update
RUN apk add nodejs
RUN apk add npm
RUN npm --registry https://registry.npm.taobao.org install pm2 -g

# 修改时区为上海
RUN apk add tzdata
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN apk del tzdata