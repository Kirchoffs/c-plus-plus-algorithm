cmake_minimum_required(VERSION 3.5)
project(c-plus-plus-algorithm LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB_RECURSE ALL_SOURCES "src/*.cpp")

foreach(source_file ${ALL_SOURCES})
    get_filename_component(executable_name ${source_file} NAME_WE)
    message(STATUS "Adding executable: ${executable_name} from ${source_file}")
    add_executable(${executable_name} ${source_file})
endforeach()
