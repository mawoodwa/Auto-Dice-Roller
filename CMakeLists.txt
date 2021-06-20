cmake_minimum_required(VERSION 3.0)
project(gtk-helloworld VERSION 1.0 LANGUAGES CXX)

find_package(PkgConfig)
pkg_check_modules(GTKMM gtkmm-3.0)

add_executable(helloworld apps/main.cpp src/helloworld.cpp)

target_include_directories(helloworld PRIVATE ${GTKMM_INCLUDE_DIRS} include)
target_link_directories(helloworld PRIVATE ${GTKMM_LIBRARY_DIRS})
target_link_libraries(helloworld ${GTKMM_LIBRARIES})
