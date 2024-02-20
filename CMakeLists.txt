cmake_minimum_required(VERSION 3.10)
project(DemoApp LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(BASE_DIRECTORY ${CMAKE_BINARY_DIR}/build/${CMAKE_BUILD_TYPE}/${CMAKE_SYSTEM_NAME}/${CMAKE_SYSTEM_PROCESSOR})

# Output directories - currently flat TBD later
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${BASE_DIRECTORY}/bin)

# Add new subdirectories here. These are executed in the
# order they are listed. So place the libraries before
# the apps that use them.
add_subdirectory(apps/SumClient)
add_subdirectory(apps/SumServer)