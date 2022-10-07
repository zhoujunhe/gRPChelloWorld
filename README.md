# 说明
这是一个C++ 使用Visual Studio 2019 工具来编译GRPC的一个hello World的例子。已经创建好项目文档，但grpc开发环境的挡建，请参照下面说明来安装，安装过程如果比较缓慢或者中断，请自行爬梯处理。

# 环境安装

本
## vcpkg安装
```
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
bootstrap-vcpkg.bat
```

初始化后，可以将vcpkg文件夹加入环境变量中，方便后面使用。


gRPC依赖库安装

```
vcpkg install grpc grpc:x64-windows
vcpkg install protobuf protobuf:x64-windows
vcpkg install protobuf[zlib] protobuf[zlib]:x64-windows
```

使安装环境变量生效
```
vcpkg integrate install
```

# 编译
使用Visual Studio 2019以上版本打开helloWorld.sln,编译整个解决方案


# 修改helloworld.proto说明

修改helloworld.proto之后，需切换到proto目录之后，运行Build.bat文件


# 运行

整个解决方案编译后，我这里配置以debug，win32平台为例子，打开cmd,切换到解决方案目录，

```
cd Debug
>helloWorldserver.exe
Server listening on 0.0.0.0:50051
```
把helloWorldClient项目设置为启动项目，直接点工作栏上三角形调试按钮进行调试。


