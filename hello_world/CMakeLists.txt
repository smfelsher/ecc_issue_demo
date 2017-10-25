cmake_minimum_required(VERSION 3.5.1 FATAL_ERROR)

# Create a project name and the language supported.
project(hello_world LANGUAGES CXX)

# Define a target name and the source files required to build the target. The appropriate extension
# (e.g. .exe on Windows, nothing on Linux) shall be applied to the file name since this is an
# executable.
add_executable(hello_world
	Main.cpp
	)

# Libraries that this target depends upon.
target_link_libraries(hello_world
	PRIVATE Print
	)

target_compile_options(hello_world
	PRIVATE -O0
	PRIVATE -g3
	PRIVATE -pedantic-errors
	PRIVATE -Wall
	PRIVATE -Wextra
	PRIVATE -Wdouble-promotion
	PRIVATE -Wmissing-include-dirs
	PRIVATE -Wunused
	PRIVATE -Wshadow
	PRIVATE -Wconversion
	PRIVATE -Wmissing-declarations
	PRIVATE -Werror
	)
