project(sample)

file(GLOB SRCS "*.c")

include_directories(${CMAKE_SOURCE_DIR}/src)

add_executable(sample ${SRCS})

target_link_libraries(sample peer)
if(NOT WIN32)
    target_link_libraries(sample pthread)
endif()

