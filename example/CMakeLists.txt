cmake_minimum_required(VERSION 3.24)

project(FormatOutput LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)

find_package(fmt REQUIRED)
find_package(ZLIB REQUIRED)

find_package(oatpp-swagger REQUIRED)
# ...



add_executable(main main.cpp)
target_link_libraries(main PRIVATE fmt::fmt)
target_link_libraries(main PRIVATE ZLIB::ZLIB)
target_link_libraries(main PRIVATE oatpp::oatpp-swagger)