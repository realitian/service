cmake_minimum_required (VERSION 2.8)
project (Service)

set (CMAKE_CXX_STANDARD 11)

add_executable (Service service.cpp ZlibUtil.cpp)

# Indicate which libraries to include during the link process.

target_link_libraries (Service -lboost_system -lopencv_core -lopencv_imgproc -lopencv_highgui -lz)

install (TARGETS Service DESTINATION bin)
