cmake_minimum_required(VERSION 3.5.1 FATAL_ERROR)

project(hello_world)

add_executable(hello_world
	Main.cpp
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

target_link_libraries(hello_world
	PRIVATE Print
	)
