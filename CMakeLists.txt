cmake_minimum_required(VERSION 3.28)
project(uWebSockets)

add_subdirectory(uSockets)

# Create interface library
add_library(uWebSockets INTERFACE)
target_include_directories(uWebSockets INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}/src
    ${CMAKE_CURRENT_SOURCE_DIR}/uSockets/src
)
# target_link_libraries(uWebSockets INTERFACE uSockets)