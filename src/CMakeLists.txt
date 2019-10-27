set(target_name dales4)
FILE(GLOB sourcefiles "*.f90")
add_executable(${target_name} ${sourcefiles})
target_link_libraries(${target_name} ${NETCDF_LIBS})
install(TARGETS dales4 DESTINATION ${PROJECT_BINARY_DIR/bin} RUNTIME DESTINATION 
        /home/paustin/paustin/repos/dales/bin )
