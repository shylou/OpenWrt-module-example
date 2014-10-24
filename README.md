OpenWrt-module-example
======================

这是一个在openwrt里添加模块的事例
---------------------------------
  开发环境是在ubuntu下，搭建好openwrt的编译环境，这里不再多讲，网上教程很多<br>
    在这里我们选择openwrt-trunk版本
    进入trunk的package文件夹创建模块目录：
    cd trunk/package
    mkdir example
    进入example目录，创建Makefile文件和代码路径:
    cd example
    touch　Makefile
    mkdir src
    进入src目录，创建代码路径和相关源文件
    cd src
    touch example.c Kconfig Makefile
    相关代码在本项目中
    回到主路径 trun编译选项配置保存并编译
    make menuconfig
    　  Kernel modules --->
      　　  Other modules --->
    　　　　　kmod-example
    　选项设置为M，保存退出
      　然后编译该模块：
    make package/example/compile</br>
