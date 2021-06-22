FROM qts8n/cuda-python:devel

LABEL maintainer="qts8n <efisher9680@gmail.com>"

# next variables are used in Makefile
# NOTE: it is important to keep them here
ARG GPU=1
ARG CUDNN=1
ARG DEBUG=0

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

