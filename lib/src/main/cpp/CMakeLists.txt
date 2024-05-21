cmake_minimum_required(VERSION 3.18.1)

project(fmjni)

add_library(fmjni
        SHARED
        fmr_core.cpp
        fmr_err.cpp
        libfm_jni.cpp
        common.cpp
)

find_library(log-lib log)
target_link_libraries(fmjni ${log-lib})
