cmake_minimum_required(VERSION 3.19)
project(Nectere)

set(NAME NectereDiscord)

set(Boost_USE_MULTITHREADED ON)
find_package(Boost 1.75.0 REQUIRED system regex)

if (Boost_FOUND)
    include_directories(${PROJECT_SOURCE_DIR})
    include_directories(${Boost_INCLUDE_DIRS})

    set(SOURCE_FILES
            ${CMAKE_CURRENT_SOURCE_DIR}/src/Discord.cpp)

    add_library(${NAME} MODULE ${SOURCE_FILES})
endif()
