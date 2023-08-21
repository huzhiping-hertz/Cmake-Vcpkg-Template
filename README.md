# CMake Vcpkg Template

# Windows Enviroment
安装编译环境
使用visual studio 2022(community)

vcpkg 安装
安装目录c:\work
git clone https://github.com/microsoft/vcpkg
cd c:\work\vcpkg
bootstrap-vcpkg.bat

# Ubuntu Enviroment
安装编译环境
apt install build-essential

vcpkg 安装
git clone https://github.com/microsoft/vcpkg

apt-get install curl zip unzip tar
apt-get install cmake
apt-get install ninja-build
./bootstrap-vcpkg.sh

将vcpkg 目录移动到/usr/local/vcpkg
/etc/profile配置

export PATH=$PATH:/usr/local/vcpkg

#vcpkg baseline 查看
git log 
commit 号对应的就是baseline 

#使用visual studio 编译

1、打开CMakePresets.json文件修该配置CMAKE_TOOLCHAIN_FILE和当前编译信息
2、使用vs 打开文件夹 CMake_Vcpkg_Template
3、vcpkg 会自动安装vcpkg.json配置的依赖(这个过程比较慢，如果有错误可以多试几次)
4、右键CMakeLists.txt 选择编译

#使用vscode 编译

该文件夹下有vcpkg.json 文件用于控制第三方依赖库
正常情况下用vscode 打开该项目后右键CMakeLists.txt 后
选择Clean Reconfigure All Projects 后自动加载第三库

#使用vscode 远程编译

1、本地安装
   remote-ssh 

2、远程安装
   c/c++ extension pack

远程安装方法
可以网上查看


#关于vcpkg install 比较慢的问题
先下载后安装
vcpkg install xxx --only-downloads
vcpkg install xxx
