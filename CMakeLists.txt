cmake_minimum_required(VERSION 4.0)
project(match3 C)

set(CMAKE_C_STANDARD 17)

# Enable Debug + Release in CLion
set(CMAKE_BUILD_TYPE Debug CACHE STRING "" FORCE)
set_property(CACHE CMAKE_BUILD_TYPE PROPERTY STRINGS "Debug" "Release")

# Headers
include_directories(${CMAKE_SOURCE_DIR}/include)

# Libraries
link_directories(${CMAKE_SOURCE_DIR}/lib)

# Copy assets folder to build directory
file(COPY assets DESTINATION ${CMAKE_BINARY_DIR})

# Executable
add_executable(match3 main.c)

# Link the import library for the DLL
target_link_libraries(match3 raylibdll)

# Copy raylib.dll next to the executable after build
add_custom_command(TARGET match3 POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different
        "${CMAKE_SOURCE_DIR}/lib/raylib.dll"
        $<TARGET_FILE_DIR:match3>
)
