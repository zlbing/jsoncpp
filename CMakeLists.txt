cmake_minimum_required(VERSION 2.8.3)
project(jsoncpp)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -fPIC -O3")

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS
)

catkin_package(
  INCLUDE_DIRS jsoncpp_dist
  LIBRARIES ${PROJECT_NAME}
)

include_directories(
  jsoncpp_dist
  ${catkin_INCLUDE_DIRS}
)

add_library(jsoncpp STATIC
    jsoncpp_dist/jsoncpp.cpp
)

target_link_libraries(${PROJECT_NAME}
 ${catkin_LIBRARIES}
)
