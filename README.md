# M625-u1

E625(F62) M625
==============

1. set up python 2

sudo -s

sudo apt install pip
pip install virtualenv
which python2.7
which python3
virtualenv -p /usr/bin/python2.7 Vpy27
source Vpy27/bin/activate

2. from then on
sudo -s

virtualenv -p /usr/bin/python2.7 Vpy27
source Vpy27/bin/activate

3.Edit makefile to 

CC=/home/grahame/toolchains/jopp/samsung-exynos9820-toolchain-default/clang/host/linux-x86/clang-4639204-cfp-jopp/bin/clang

4. Build

make clean && make mrproper
export CROSS_COMPILE= ~/toolchains/aarch64-linux-android-4.9-master/bin/aarch64-linux-android-
export ARCH=arm64
export PLATFORM_VERSION=11
export ANDROID_MAJOR_VERSION=r
make physwizz_defconfig
make 
