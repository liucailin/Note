在centos编译skynet的时候，会报错**fatal error: stdatomic.h: No such file or directory**，原因是gcc版本太老了，4.8。

升级办法

yum -y install centos-release-scl
yum -y install devtoolset-8-gcc devtoolset-8-gcc-c++ devtoolset-8-binutils
scl enable devtoolset-8 bash

需要注意的是scl命令启用只是临时的，退出shell或重启就会恢复原系统gcc版本。
如果要长期使用gcc 8.3的话：

echo "source /opt/rh/devtoolset-8/enable" >>/etc/profile



https://www.vpser.net/manage/centos-6-upgrade-gcc.html