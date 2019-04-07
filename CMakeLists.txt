# CMakeList.txt : CMake project for CMakeProject, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

set(CMAKE_CXX_STANDARD 11)

find_package(Torch REQUIRED)

# Add source to this project's executable.
add_executable (CMakeProject "Source.cpp")
target_link_libraries(CMakeProject ${TORCH_LIBRARIES})
target_include_directories(CMakeProject PUBLIC ${TORCH_INCLUDE_DIRS})
# TODO: Add tests and install targets if needed.
