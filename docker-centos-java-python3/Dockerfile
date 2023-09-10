FROM centos:7

RUN yum update -y && \
    yum install -y wget gcc make zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel libffi-devel xz-devel

RUN wget https://www.python.org/ftp/python/3.9.17/Python-3.9.17.tgz && \
    tar xzf Python-3.9.17.tgz && \
    cd Python-3.9.17 && \
    ./configure --enable-optimizations && \
    make altinstall && \
    cd .. && \
    rm -rf Python-3.9.17* && \
    ln -s /usr/local/bin/python3.9 /usr/bin/python3 && \
    ln -s /usr/local/bin/pip3.9 /usr/bin/pip3

RUN yum install -y java-1.8.0-openjdk

ENV PATH="/usr/local/bin:${PATH}"
