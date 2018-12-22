cmake_minimum_required(VERSION 2.8)
project(CV)

IF(NOT CMAKE_BUILD_TYPE)
SET(CMAKE_BUILD_TYPE Debug)
ENDIF()

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

find_package(OpenCV REQUIRED)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -O3 -march=native ")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -O3 -march=native -std=c++11 -Wno-reorder")

include_directories(
${PROJECT_SOURCE_DIR}/
)

add_executable(imageload imageload.cpp)
target_link_libraries(imageload 
${OpenCV_LIBS})

add_executable(gms gms.cpp)
target_link_libraries(gms 
${OpenCV_LIBS})

add_executable(visualodom visualodom.cpp)
target_link_libraries(visualodom 
${OpenCV_LIBS})

add_executable(visualodomfunc visualodomfunc.cpp)
target_link_libraries(visualodomfunc 
${OpenCV_LIBS})

add_executable(visualodomforkitti visualodomforkitti.cpp)
target_link_libraries(visualodomforkitti 
${OpenCV_LIBS})

add_executable(visualodomklt visualodomklt.cpp)
target_link_libraries(visualodomklt
${OpenCV_LIBS})

add_executable(votriangulate votriangulate.cpp)
target_link_libraries(votriangulate
${OpenCV_LIBS})

add_executable(vofinal vofinal.cpp)
target_link_libraries(vofinal
${OpenCV_LIBS})

add_executable(voalltracking voalltracking.cpp)
target_link_libraries(voalltracking
${OpenCV_LIBS})

add_executable(vofinalkitti2 vofinalkitti2.cpp)
target_link_libraries(vofinalkitti2
${OpenCV_LIBS})

add_executable(vofinalkitti3 vofinalkitti3.cpp)
target_link_libraries(vofinalkitti3
${OpenCV_LIBS})

add_executable(vofinalkitti4 vofinalkitti4.cpp)
target_link_libraries(vofinalkitti4
${OpenCV_LIBS})

add_executable(vofinalkitti5 vofinalkitti5.cpp)
target_link_libraries(vofinalkitti5
${OpenCV_LIBS})
