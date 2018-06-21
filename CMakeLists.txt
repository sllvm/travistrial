cmake_minimum_required(VERSION 3.9.2)
if(MSVC)
	add_compile_options(/W4)
else()
	add_compile_options(-g -pedantic-errors -Wall -Wextra -Wpedantic)
endif()

project("intro")
add_executable(intro main.cpp ) 
target_compile_features(intro PRIVATE cxx_lambda_init_captures) #c++14

