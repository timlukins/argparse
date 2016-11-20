cmake_minimum_required (VERSION 3.0)

project (argparse VERSION 1.0.0 LANGUAGES C)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -c -Wmissing-prototypes -Wstrict-prototypes")

set(LIBRARY_NAME argparse)

set(SRC_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/argparse.c
)

set(INCLUDE_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/argparse.h
)

add_library(
    ${LIBRARY_NAME}
    STATIC
    ${SRC_FILES}
    ${INCLUDE_FILES}
)

install(TARGETS ${LIBRARY_NAME} DESTINATION lib)
install(FILES ${INCLUDE_FILES} DESTINATION include)
