# 两个重要链接

[OpenCV](https://opencv.org/releases/)

[opencv_contrib](https://github.com/opencv/opencv_contrib)

# 只安装OpenCV

只安装官方模块，即只对OpenCV源代码进行编译和安装。从[OpenCV](https://opencv.org/releases/)下载OpenCV源代码

```shell
# unpack sources
unzip opencv-4.10.0
# Create build directory
mkdir -p build && cd build

# Configure
cmake ../opencv-4.10.0

# Build
make -j$(nproc)

# Install
sudo make install
```

# 三方库+OpenCV

还是先从OpenCV下载源码

下载三方库

```shell
git clone https://github.com/opencv/opencv_contrib.git
```

编译安装

```shell
# unpack sources
unzip opencv-4.10.0
# Create build directory
mkdir -p build && cd build

# Configure
cmake -DOPENCV_EXTRA_MODULES_PATH=../opencv_contrib/modules ../opencv-4.10.0

# Build
make -j$(nproc)

# Install
sudo make install
```

