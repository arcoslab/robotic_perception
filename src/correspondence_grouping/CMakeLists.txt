cmake_minimum_required(VERSION 3.7)
project(correspondence_grouping)
find_package( PCL REQUIRED )
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -march=native")
add_executable(correspondence_grouping correspondence_grouping.cpp)

target_include_directories(${PROJECT_NAME} SYSTEM PUBLIC
                          ${PCL_INCLUDE_DIRS}
                          )

target_link_libraries(${PROJECT_NAME}
                      ${PCL_LIBRARIES}
                      )
set(CMAKE_BUILD_TYPE Debug)
