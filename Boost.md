# 清理之前的环境

```shell
sudo apt-get purge libboost-*
sudo apt-get autoremove
```

# 安装配置

**先去官网下源代码**

https://www.boost.org/users/download/

**编译并安装**

```shell
# 解压
tar -zxvf boost boost_1_85_0.tar.gz
cd boost boost_1_85_0
# 编译、安装
./bootstrap.sh --prefix=/usr
./b2 
sudo ./b2 install
```

