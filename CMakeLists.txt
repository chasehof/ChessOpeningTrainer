cmake_minimum_required(VERSION 3.10)
project(OpeningTrainer)

set(CMAKE_CXX_STANDARD 17)


include_directories(include)

file(GLOB SOURCES "src/*.cpp")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/build/bin)
add_executable(OpeningTrainer ${SOURCES})

