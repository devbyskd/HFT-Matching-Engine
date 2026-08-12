cmake_minimum_required(VERSION 3.20)
project(HFT_Matching_Engine VERSION 0.1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Optimized release flags for HFT
set(CMAKE_CXX_FLAGS_RELEASE "-O3 -march=native -flto -DNDEBUG")

add_executable(hft_engine
    src/main.cpp
)

target_include_directories(hft_engine PRIVATE include)
