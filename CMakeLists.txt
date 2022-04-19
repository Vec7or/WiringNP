cmake_minimum_required(VERSION 3.16)

project(wiringNP VERSION "0.8.0" LANGUAGES C)

file(GLOB ${PROJECT_NAME}_SOURCES ${PROJECT_SOURCE_DIR}/wiringPi/*.c)
add_library(${PROJECT_NAME}
        STATIC
        ${${PROJECT_NAME}_SOURCES})
target_include_directories(
        ${PROJECT_NAME}
        PRIVATE
        ./wiringPi/
)
