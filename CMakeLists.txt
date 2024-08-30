#1. specify the CMake minimum version
cmake_minimum_required(VERSION 3.19)

#Import pico-sdk librairie
set(FETCHCONTENT_QUIET FALSE)
set(PICO_SDK_FETCH_FROM_GIT ON)
set(PICO_SDK_FETCH_FROM_GIT_PATH ${CMAKE_CURRENT_LIST_DIR}/pico-sdk)
set(PICO_TOOLCHAIN_PATH "${PICO_TOOLCHAIN_PATH}" CACHE INTERNAL "")

#2. include the pico sdk here
include(pico_sdk_import.cmake)

#3. Specify the project name
project(1.8inch_TFT)

#4. initialize the pico sdk
pico_sdk_init()

#5. add executable
add_executable(1.8inch_TFT
    src/main.c
)

pico_enable_stdio_usb(1.8inch_TFT 1)
pico_enable_stdio_uart(1.8inch_TFT 0)

#6. Add extra outputs to the blink project
pico_add_extra_outputs(1.8inch_TFT)

#7. add target libraries
target_link_libraries(1.8inch_TFT Lib)

add_subdirectory(lib)