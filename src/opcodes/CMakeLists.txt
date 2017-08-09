add_definitions(
	-DHAVE_CONFIG_H
	-D_GNU_SOURCE
)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}
	${CMAKE_CURRENT_SOURCE_DIR}/../bfd
	${CMAKE_CURRENT_SOURCE_DIR}/../include
	${CMAKE_CURRENT_SOURCE_DIR}/../intl
)

set(opcodes_srcs
	dis-buf.c
	disassemble.c
	dis-init.c
	i386-dis.c
	i386-opc.c
	ppc-dis.c
	ppc-opc.c
)

add_library(opcodes OBJECT ${opcodes_srcs})

