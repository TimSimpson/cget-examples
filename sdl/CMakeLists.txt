project(cget_sdl_example CXX)
cmake_minimum_required(VERSION 3.2 FATAL_ERROR)

link_directories(${CMAKE_PREFIX_PATH}/lib)

add_executable(hi_sdl ${CMAKE_CURRENT_SOURCE_DIR}/src/hi_sdl.cpp)
target_link_libraries(hi_sdl SDL2 SDL2main winmm Version Imm32)

if (WIN32)
    target_link_libraries(hi_sdl winmm Version Imm32)
endif()
