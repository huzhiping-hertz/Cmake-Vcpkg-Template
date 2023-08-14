# CMake Vcpkg Template

# Windows Enviroment

# Ubuntu Enviroment
安装编译环境

apt install build-essential

第三方管理工具　VCPKG

vcpkg 依赖库安装

首先安装vcpkg
在github 上查看安装方法 

git clone https://github.com/microsoft/vcpkg

apt-get install curl zip unzip tar
apt-get install cmake
apt-get install ninja-build
./bootstrap-vcpkg.sh

将vcpkg 目录移动到/usr/local/vcpkg
/etc/profile配置

export PATH=$PATH:/usr/local/vcpkg

当前baseline 查看
git log 
commit 下对应的baseline 

cd CMake_Vcpkg_Template

打开CMakePresets.json文件修该配置CMAKE_TOOLCHAIN_FILE
和当前编译信息

该文件夹下有vcpkg.json 文件用于控制第三方依赖库
正常情况下用vscode 打开该项目后右键CMakeLists.txt 后
选择Clean Reconfigure All Projects 后自动加载第三库


远程调试
vscode 远程调试

本地安装
remote-ssh 

远程安装
c/c++ extension pack

远程安装方法
可以网上查看


关于vcpkg install 比较慢的问题
先下载后安装
vcpkg install xxx --only-downloads
vcpkg install xxx
