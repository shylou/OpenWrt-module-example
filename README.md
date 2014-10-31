OpenWrt-module-example
======================

这是一个在openwrt里添加模块的事例
---------------------------------
  开发环境是在ubuntu下，搭建好openwrt的编译环境，这里不再多讲，网上教程很多<br>
    在这里我们选择openwrt-trunk版本<br>
    进入trunk的package文件夹创建模块目录：<br>
    cd trunk/package<br>
    mkdir example<br>
    进入example目录，创建Makefile文件和代码路径:<br>
    cd example<br>
    touch　Makefile<br>
    mkdir src<br>
    进入src目录，创建代码路径和相关源文件<br>
    cd src<br>
    touch example.c Kconfig Makefile<br>
    相关代码在本项目中<br>
    回到主路径 trun编译选项配置保存并编译<br>
    make menuconfig<br>
     Kernel modules---> <br> 
       other moudles---> <br>
      　 kmod-example---> <br>
    　选项设置为M，保存退出<br>
      　然后编译该模块：<br>
    make package/example/compile<br>
