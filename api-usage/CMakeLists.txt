project(main)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/runtime)
#aux_source_directory(. Main.cpp)
add_executable(${PROJECT_NAME}
        #${DIR_SRCS}
        Main.cpp
        )
target_link_libraries(${PROJECT_NAME}
        sub:libpict
        )