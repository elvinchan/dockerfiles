FROM tensorflow/tensorflow:1.14.0-py3

LABEL maintainer "nszr90 <elvinchan@foxmail.com>"

RUN apt-get update && apt-get install -y \
    wget \
    unzip \
    zip \
    libsm6 \
    libxrender1 \
    libxext-dev \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*
RUN wget -O protobuf.zip https://github.com/google/protobuf/releases/download/v3.8.0/protoc-3.8.0-linux-x86_64.zip && \
    unzip protobuf.zip -d proto3 && \
    mv proto3/bin/* /usr/local/bin && \
    mv proto3/include/* /usr/local/include && \
    rm -rf proto3 protobuf.zip