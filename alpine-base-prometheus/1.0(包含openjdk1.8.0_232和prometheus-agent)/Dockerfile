FROM alpine:latest
MAINTAINER WeiguoLiu <liuwg-a@glodon.com>
USER root

RUN apk update
# 添加jdk
RUN apk add openjdk8
# 切到服务所在目录
RUN mkdir -p /data/service
WORKDIR /data/service
# 添加prometheus-agent
RUN wget https://gjw-prod-static.oss-cn-beijing.aliyuncs.com/test/jmx_prometheus_javaagent-0.12.0.jar
# 添加下载配置文件
RUN wget https://gjw-prod-static.oss-cn-beijing.aliyuncs.com/test/tomcat.yaml -O config.yaml
