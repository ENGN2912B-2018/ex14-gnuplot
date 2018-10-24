cmake_minimum_required(VERSION 3.2.2)

project(gnuplot)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME OFF)
find_package(Boost 1.45.0 COMPONENTS iostreams system filesystem)

if(Boost_FOUND)
    include_directories(${Boost_INCLUDE_DIRS})
    add_executable(ex1 src/example1.cpp)
    target_link_libraries(ex1 ${Boost_LIBRARIES})
    target_include_directories(ex1 PUBLIC lib)
endif()

#include_directories(src)

# add_library(random
# 	lib/firfilter.hpp
#     lib/firfilter.cpp
# )
#set_target_properties(ex1 PROPERTIES LINKER_LANGUAGE CXX)

# add_executable(ex1 src/example1.cpp)
#add_executable(ex2 src/example2.cpp)

# target_link_libraries(ex1 ${Boost_LIBRARIES})

# target_include_directories(ex1 PUBLIC lib)
#target_include_directories(ex2 PUBLIC lib)
