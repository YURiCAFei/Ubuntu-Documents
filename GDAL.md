# 安装两个重要的依赖项

## sqlite3

```shell
sudo apt-get install sqlite3
```

## proj

<font color=red>一定要先安装sqlite3再安装proj</font>

**先下载**

下载地址 [download.osgeo.org/proj/](https://link.juejin.cn?target=https%3A%2F%2Fdownload.osgeo.org%2Fproj%2F)

```c++
wget https://download.osgeo.org/proj/proj-9.3.1.tar.gz
tar -zxvf proj-9.3.1.tar.gz
```

**编译安装**

```shell
cd proj-9.3.1/
sudo apt-get install sqlite3 libsqlite3-dev libtiff-dev libcurl4-openssl-dev
mkdir build
cd build
cmake .. #运行 CMake 配置
make -j$(nproc)    #运行 make 构建项目
sudo make install #安装项目
```

# 配置GDAL

**老规矩，先[下载](https://gdal.org/en/latest/download.html#source-code)**

可以用wget，也可以在浏览器下载

**配置、安装**

```shell
# 解压
tar -zxvf gdal-3.9.2.tar.gz
cd gdal-3.9.2.tar.gz
mkdir build
cd build
cmake .. #运行 CMake 配置
make -j$(nproc)    #运行 make 构建项目
sudo make install #安装项目
```

