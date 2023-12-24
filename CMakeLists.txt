cmake_minimum_required(VERSION 3.14.0)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -target x86_64-w64-mingw32")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -target x86_64-w64-mingw32")

project(tests)

include_directories(c:/users/paul/.conda/envs/xtensorstacktest/Library/include)
link_directories(c:/users/paul/.conda/envs/xtensorstacktest/Library/lib)

add_executable(tests tests.cpp)
target_link_libraries(tests
	PUBLIC libreflapack_wu
	PUBLIC libreflapack_nu
	PUBLIC libblas_REF_nu
	PUBLIC libblas_REF_wu
	PUBLIC cblas_nu
	PUBLIC cblas_wu
	PUBLIC gfortran
	PUBLIC stdc++)
