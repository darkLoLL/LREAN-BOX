# CMake

## PROJECT关键字

指定工程的名字、支持预言，默认所有预言

PROJECT(NAME [C] [CXX] [JAVA])

## SET关键字

SET(SRC main.cpp)

SRC变量中包含main.cpp

## MESSAGE关键字

输出一些自定义信息

MESSSAGE()

SEND_ERROR，产生错误，生产过程跳过

SATUS，输出前缀$-$的信息

FATAL_ERROR，终止所有cmake进程

## add_executable

生成可执行文件

add_executable(\${PROJECT_NAME} \${SRC})

# 语法基本原则

变量使用\${}方式获取值，在IF控制语句中可直接使用变量名

指令（参数1 参数2 ...）参数间可以使用空格、分号分开

指令大小写无关，参数和变量区分大小写

# 内部构建和外部构建

## 外部构建



```
mkdir build
cd build
cmake ..
make
```

## 让代码更像一个工程

### 将目标文件放入bin子目录

```
.
build
CmakeLists.txt
src
	main.cpp
	CMakeLists.txt
```

在工程下的$CMakeLists.txt$

```
project(hello)
add_subdirectory(src bin)
# bin生成的文件放入bin目录
```

在src目录下的$CMakeLists.txt$

```
add_executable(${PROJECT_NAME} ${SRC})
```

## 使用CMake安装

make install DESTDIR=

```
目录树
.
build
CmakeLists.txt
COPYRIGHT
doc
	hello.txt
README
runhello.sh
src
	main.cpp
	CMakeLists.txt
```

> 安装文件COPYRIGHT和README
>
> install(FILES COPYRIGHT README DESTINATION share/doc/cmake/)

> 安装脚本
>
> install(PROGRAMS runhello.sh  DESTINATION bin)

> 安装doc中的hello.txt
>
> install(DIRECTORY doc/ DESTINATION share/doc/cmake)

## 构建静态库

```c
.
    build
    CMakeLists.txt
    lib
    	CMakeLists.txt
    	hello.cpp
    	hello.h
```

在工程下的$CMakeLists.txt$

```
project(hello)
add_subdirectory(lib bin)
# bin生成的文件放入bin目录
```

在$lib$目录下的$CMakeLists.txt$

```
add_library(${NAME} SHARE hello.cpp)
```

## add_library

SHARE，动态库

STATIC，静态库

## 指定输出路径
```cmake
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/bin)  
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/bin)  
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/lib)
```
