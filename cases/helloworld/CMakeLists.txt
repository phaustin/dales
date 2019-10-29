cmake_minimum_required(VERSION 3.1)
PROJECT(hello Fortran)
set(target_name helloworld)
FILE(GLOB sourcefiles "*.f90")
add_executable(${target_name} ${sourcefiles})
set(dir "$ENV{HOME}")
message("pha creating folder ${dir}/bin if it doen't exist")
SET(CMAKE_INSTALL_PREFIX "${dir}")
install(DIRECTORY DESTINATION "${dir}/bin")
install(TARGETS helloworld)


