cmake_minimum_required(VERSION 3.5)
project(Auto-Dice-Roller)

add_executable(helloworld helloworld.cpp)

find_package(wxWidgets REQUIRED)
include(${wxWidgets_USE_FILE})
add_executable(gui gui.cpp)
target_link_libraries(gui ${wxWidgets_LIBRARIES})
