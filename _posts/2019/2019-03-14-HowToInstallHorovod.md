---
layout: post
title:  "How To Install Horovod on Ubuntu 18.04"
date:   2019-03-14
excerpt: "How To Install Horovod"
feature: ../../posts/feature/2019-03-14-HowToInstallHorovod.jpg
tag:
- Horovod
- Multi-GPU
- OpenMPI
comments: true
---

# How To Install Horovod (on Ubuntu 18.04)

## Index

- [Install OpenMPI](#install-openmpi)
- [Install Horovod](#install-horovod)

## Install OpenMPI

1.&nbsp;Download OpenMPI

~~~ shell
wget https://download.open-mpi.org/release/open-mpi/v4.0/openmpi-4.0.0.tar.gz
~~~

2.&nbsp;Install OpenMPI

~~~ shell
tar -xzvf openmpi-4.0.0.tar.gz
cd openmpi-4.0.0
./configure --prefix=/usr/local --with-cuda
sudo make all install
~~~

3.&nbsp;run ldconfig

~~~ shell
sudo ldconfig
~~~

## Install Horovod

~~~ shell
HOROVOD_GPU_ALLREDUCE=NCCL sudo -H pip2 install --no-cache-dir horovod
~~~

or

~~~ shell
HOROVOD_GPU_ALLREDUCE=NCCL sudo -H pip3 install --no-cache-dir horovod
~~~
