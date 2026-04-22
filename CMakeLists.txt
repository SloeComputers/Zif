#-------------------------------------------------------------------------------
# Copyright (c) 2019 John D. Haughton
# SPDX-License-Identifier: MIT
#-------------------------------------------------------------------------------

cmake_minimum_required(VERSION 3.20)

project(Zif
        LANGUAGES CXX
        VERSION 0.6.2)

if(NOT DEFINED BUILD_TESTING)
    set(BUILD_TESTING OFF CACHE BOOL "Build unit tests")
endif()
include(CTest)

add_subdirectory(PDK)
add_subdirectory(Source)

#-------------------------------------------------------------------------------

install(TARGETS zif RUNTIME DESTINATION .)
install(FILES README DESTINATION .)
install(DIRECTORY Images DESTINATION .)
install(DIRECTORY Games DESTINATION .)
install(DIRECTORY Scripts DESTINATION .)
