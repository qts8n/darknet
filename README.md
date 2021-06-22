# Darknet

##### Object detection neural network framework

Darknet is an open source neural network framework written in C and CUDA.
It is fast, easy to install, and supports CPU and GPU computation.

This fork adds the possibility to pass a callback function in the training pipeline
for logging purposes and fixes a bunch of memory leaks in the training process.

It adds the support of recent RTX architectures and Dockerfiles to use as a base of
your projects.

Dockerfiles are based on on `devel` tags of `qts8n/cuda-python` image.
It has `cuda-9.1` and `cuda-10.2` tags with support of CUDA 9.1 and CUDA 10.2 versions respectively.

## References

see: [Darknet](https://github.com/pjreddie/darknet) github

see: [Darknet project](http://pjreddie.com/darknet) website

see: [qts8n/cuda-python](https://hub.docker.com/r/qts8n/cuda-python) docker-hub

see: [nvidia/cuda](https://hub.docker.com/r/nvidia/cuda) docker-hub

