cmake_minimum_required(VERSION 3.5)

project(helloworld)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if (MSVC)
    add_compile_options(/utf-8)
endif()

file(GLOB ROOT_HEADERS *.h)
file(GLOB ROOT_SOURCES *.cpp)

source_group(helloworld FILES
  ${ROOT_HEADERS}
  ${ROOT_SOURCES}
)

add_executable(helloworld
  ${ROOT_HEADERS}
  ${ROOT_SOURCES}
)
