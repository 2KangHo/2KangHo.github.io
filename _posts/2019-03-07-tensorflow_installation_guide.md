---
layout: post
title:  "tensorflow installation guide"
date:   2019-03-07
excerpt: "Guide of installing tensorflow"
tag:
- Ubuntu18.04
- tensorflow1.13
comments: true
---


# tensorflow installation guide

```shell
sudo cp /usr/lib/x86_64-linux-gnu/libcublas.so.10.1.0.105 /usr/local/cuda-10.1/lib64/
sudo ln -s /usr/local/cuda-10.1/lib64/libcublas.so.10.1.0.105 /usr/local/cuda-10.1/lib64/libcublas.so.10.1
sudo ln -s /usr/local/cuda-10.1/lib64/libcublas.so.10.1 /usr/local/cuda-10.1/lib64/libcublas.so
sudo ln -s /usr/local/cuda-10.1/targets/x86_64-linux/lib/libcusolver.so.10 /usr/local/cuda-10.1/lib64/libcusolver.so.10.1
sudo ln -s /usr/local/cuda-10.1/targets/x86_64-linux/lib/libcurand.so.10 /usr/local/cuda-10.1/lib64/libcurand.so.10.1
sudo ln -s /usr/local/cuda-10.1/targets/x86_64-linux/lib/libcufft.so.10 /usr/local/cuda-10.1/lib64/libcufft.so.10.1
```


```
You have bazel 0.19.2 installed.
Please specify the location of python. [Default is /usr/bin/python]: /usr/bin/python3


Found possible Python library paths:
  /usr/lib/python3/dist-packages
  /usr/local/lib/python3.6/dist-packages
Please input the desired Python library path to use.  Default is [/usr/lib/python3/dist-packages]

Do you wish to build TensorFlow with XLA JIT support? [Y/n]: y
XLA JIT support will be enabled for TensorFlow.

Do you wish to build TensorFlow with OpenCL SYCL support? [y/N]: n
No OpenCL SYCL support will be enabled for TensorFlow.

Do you wish to build TensorFlow with ROCm support? [y/N]: n
No ROCm support will be enabled for TensorFlow.

Do you wish to build TensorFlow with CUDA support? [y/N]: y
CUDA support will be enabled for TensorFlow.

Please specify the CUDA SDK version you want to use. [Leave empty to default to CUDA 10.0]: 10.1


Please specify the location where CUDA 10.1 toolkit is installed. Refer to README.md for more details. [Default is /usr/local/cuda]: 


Please specify the cuDNN version you want to use. [Leave empty to default to cuDNN 7]: 7.5.0


Please specify the location where cuDNN 7 library is installed. Refer to README.md for more details. [Default is /usr/local/cuda]: 


Do you wish to build TensorFlow with TensorRT support? [y/N]: n
No TensorRT support will be enabled for TensorFlow.

Please specify the locally installed NCCL version you want to use. [Default is to use https://github.com/nvidia/nccl]: 2.4.2


NCCL libraries found in /usr/lib/x86_64-linux-gnu/libnccl.so
This looks like a system path.
Assuming NCCL header path is /usr/include
Please specify a list of comma-separated Cuda compute capabilities you want to build with.
You can find the compute capability of your device at: https://developer.nvidia.com/cuda-gpus.
Please note that each additional compute capability significantly increases your build time and binary size. [Default is: 6.1,6.1,6.1]: 


Do you want to use clang as CUDA compiler? [y/N]: n
nvcc will be used as CUDA compiler.

Please specify which gcc should be used by nvcc as the host compiler. [Default is /usr/bin/gcc]: 


Do you wish to build TensorFlow with MPI support? [y/N]: n
No MPI support will be enabled for TensorFlow.

Please specify optimization flags to use during compilation when bazel option "--config=opt" is specified [Default is -march=native -Wno-sign-compare]: -march=native


Would you like to interactively configure ./WORKSPACE for Android builds? [y/N]: n
Not configuring the WORKSPACE for Android builds.
```