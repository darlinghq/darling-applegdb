project(gdb-top)

add_definitions(-D_DARWIN_UNLIMITED_STREAMS)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -nostdinc")

add_subdirectory(src/libiberty)
add_subdirectory(src/bfd)
add_subdirectory(src/opcodes)
add_subdirectory(src/intl)
add_subdirectory(src/readline)
add_subdirectory(src/gdb)

