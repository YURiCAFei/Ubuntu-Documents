# 获取源代码

[get ceres-2.2.0](http://ceres-solver.org/ceres-solver-2.2.0.tar.gz) 

# 安装依赖

下面是官网要求的依赖，可根据实际情况进行安装

```shell
# CMake
sudo apt-get install cmake
# google-glog + gflags
sudo apt-get install libgoogle-glog-dev libgflags-dev
# Use ATLAS for BLAS & LAPACK
sudo apt-get install libatlas-base-dev
# Eigen3
sudo apt-get install libeigen3-dev
# SuiteSparse (optional)
sudo apt-get install libsuitesparse-dev
```

# 编译并安装库

```shell
ar zxf ceres-solver-2.2.0.tar.gz
mkdir ceres-bin
cd ceres-bin
cmake ../ceres-solver-2.2.0
make -j$(nproc)
make test
sudo make install
```

