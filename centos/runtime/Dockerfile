ARG repository
ARG version
FROM ${repository}:${version}-centos-base
LABEL maintainer "Wang Qiang <wangqiang8511@gmail.com>"

RUN yum install -y \
        cuda-libraries-$CUDA_PKG_VERSION && \
    rm -rf /var/cache/yum/*
