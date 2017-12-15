ARG repository
ARG version
FROM ${repository}:${version}-ubuntu-base
LABEL maintainer "Wang Qiang <wangqiang8511@gmail.com>"

RUN apt-get update && apt-get install -y --no-install-recommends \
        cuda-libraries-$CUDA_PKG_VERSION && \
    rm -rf /var/lib/apt/lists/*
