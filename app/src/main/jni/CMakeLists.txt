project(yolov5ncnn)

cmake_minimum_required(VERSION 3.10)

set(ncnn_DIR /Users/liuqiaoping/Documents/github/ncnn/build-android-aarch64/install/lib/cmake/ncnn)
find_package(ncnn REQUIRED)

add_library(yolov5ncnn SHARED yolov5ncnn_jni.cpp)

target_link_libraries(yolov5ncnn
    ncnn

    jnigraphics
)
