cmake_minimum_required(VERSION 3.1)
set(target_name helloworld)
set(CMAKE_Fortran_COMPILER mpif90)
enable_language(Fortran)
FILE(GLOB sourcefiles "*.f90")
add_executable(${target_name} ${sourcefiles})
set(dir "$ENV{HOME}")
message("pha creating folder ${dir}/bin if it doen't exist")
SET(CMAKE_INSTALL_PREFIX "${dir}")
install(DIRECTORY DESTINATION "${dir}/bin")
install(TARGETS helloworld)


