# Termux安装opencv的方法


> 原文地址 https://blog.csdn.net/baby_moon/article/details/81070638

### 1.安装 python3 和 dev

> pkg install python python-dev
----------
### 2.安装 tools 和 libs
>pkg install libjpeg-turbo-dev libpng-dev cmake pkg-config
----------
### 3.在git克隆opencv
>git clone https://github.com/opencv/opencv && cd opencv
----------
### 4.创建生成目录
>mkdir build && cd build
----------
### 5.配置
>LDFLAGS=" -llog -lpython3" cmake -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_INSTALL_PREFIX=$PREFIX -DBUILD_opencv_python3=on -DBUILD_opencv_python2=off -DWITH_QT=OFF -DWITH_GTK=OFF ..

----------
### 6.编译
>make

>make install
----------
### 7.用python测试
>import cv2

>cv2.__version__
----------
