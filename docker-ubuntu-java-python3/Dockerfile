FROM ubuntu:20.04

# 设置Python和Java和基本系统
ENV DEBIAN_FRONTEND noninteractive
ENV LANG=en_US.UTF-8

RUN apt-get update && \
  apt-get upgrade -y && \
  apt-get install -q -y openjdk-8-jdk python3-pip libsnappy-dev language-pack-en supervisor

RUN pip3 install --upgrade pip requests

ADD supervisord.conf /etc/supervisor/supervisord.conf