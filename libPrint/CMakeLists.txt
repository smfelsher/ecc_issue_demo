cmake_minimum_required(VERSION 3.5.1 FATAL_ERROR)

project(libPrint)

add_library(Print
	Print.cpp
	)

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

target_include_directories(Print
	PUBLIC include
	)
