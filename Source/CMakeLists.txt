#-------------------------------------------------------------------------------
# Copyright (c) 2019 John D. Haughton
# SPDX-License-Identifier: MIT
#-------------------------------------------------------------------------------

add_executable(zif
               zif.cpp
               common/ConsoleImpl.cpp)

target_compile_definitions(zif PRIVATE TERMINAL_EMULATOR)

target_include_directories(zif PRIVATE .)

target_link_libraries(zif PRIVATE GUI PLT)

set_target_properties(zif PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}")
