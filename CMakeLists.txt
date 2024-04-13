cmake_minimum_required(VERSION 3.15)

project(kdmapper)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(kdmapper/include)

add_executable(
    ${PROJECT_NAME}
        kdmapper/src/main.cpp
        kdmapper/src/kdmapper.cpp
        kdmapper/src/portable_executable.cpp
        kdmapper/src/utils.cpp
        kdmapper/src/service.cpp
        kdmapper/src/intel_driver.cpp
)

target_include_directories(
    ${PROJECT_NAME}
        PRIVATE
            kdmapper/include
)