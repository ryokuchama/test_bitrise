cmake_minimum_required(VERSION 3.22)

# set(CMAKE_C_COMPILER "usr/bin/clang")
# set(CMAKE_CXX_COMPILER "usr/bin/clang++")

project(IntercomCommonLib)

# C++17で固定
set(CMAKE_CXX_STANDARD 17)

message("Build for Yocto")
set(CMAKE_SYSTEM_NAME Linux)
set(CMAKE_SYSTEM_PROCESSOR ARM)
set(CMAKE_C_COMPILER clang)
set(CMAKE_CXX_COMPILER clang++)

add_library(sample_linux STATIC src/test.cpp)

# iOSの場合
# if (APPLE)
# message("Build for iOS")
# set(PLATFORM_NAME "iOS")
# add_library(sample_ios STATIC src/test.cpp)

# elseif(ANDROID)
# message("Build for Android")
# set(PLATFORM_NAME "Android")
# add_library(sample_android STATIC src/test.cpp)

# else(APPLE)
# message("Build for Yocto")
# set(CMAKE_SYSTEM_NAME Linux)
# add_library(sample_linux STATIC src/test.cpp)

# endif(APPLE)
