FROM qts8n/cuda-python:devel

LABEL maintainer="qts8n <efisher9680@gmail.com>"

ENV BUILD_DIR=/root/temp
ENV SRC_DIR=/usr/src/darknet

# preparing for the build
RUN mkdir "$BUILD_DIR" \
    && mkdir -p "$SRC_DIR"

COPY . "$BUILD_DIR"

# building darknet lib
RUN cd "$BUILD_DIR" \
    && make -j$(nproc) \
    && cp libdarknet.so "$SRC_DIR" \
    && cd ~ \
    && rm -rf "$BUILD_DIR"

