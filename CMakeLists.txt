cmake_minimum_required(VERSION 3.16)
project("ARFF")

include_directories("src")
file(GLOB SRC_FILES "src/*.cpp")

add_library("ARFF" STATIC ${SRC_FILES} )
add_subdirectory("tests")
