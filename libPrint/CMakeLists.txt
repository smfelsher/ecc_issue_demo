cmake_minimum_required(VERSION 3.5.1 FATAL_ERROR)

# Create a project name and the language supported.
project(libPrint LANGUAGES CXX)

# Define a target name and the source files required to build the target. The appropriate prefix
# (e.g. lib) and extension (e.g. .a, .so, .dll) shall be applied to the output filename since this
# is a library.
add_library(Print
	src/Print.cpp
	)

# Set include directories. PUBLIC headers are used for compiling the library and will be added to a
# consumer's include search path.
target_include_directories(Print
	PUBLIC include
	)

# Set the options for compiling this library.
target_compile_options(Print
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
