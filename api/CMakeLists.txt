add_compile_options(-fPIC -Iapi -w -fpermissive)
project(pict)
aux_source_directory(. DIR_PVSIMLIB_SRCS)
add_library(${PROJECT_NAME} ${DIR_PVSIMLIB_SRCS})
add_library(sub::libpict ALIAS ${PROJECT_NAME})
set(CMAKE_CXX_STANDARD 11)
target_include_directories( ${PROJECT_NAME}
        PUBLIC ${PROJECT_SOURCE_DIR})