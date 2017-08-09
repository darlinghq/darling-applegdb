add_definitions(-DHAVE_CONFIG_H)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}
	${CMAKE_CURRENT_SOURCE_DIR}/../include
	${CMAKE_CURRENT_SOURCE_DIR}/../intl
)

set(extra_arch_defs "-DDEFAULT_VECTOR=mach_o_le_vec -DSELECT_VECS='&mach_o_le_vec,&mach_o_be_vec,&mach_o_fat_vec,&pef_vec,&pef_xlib_vec,&sym_vec' -DSELECT_ARCHITECTURES='&bfd_i386_arch,&bfd_powerpc_arch,&bfd_rs6000_arch' -DHAVE_mach_o_le_vec -DHAVE_mach_o_be_vec -DHAVE_mach_o_fat_vec -DHAVE_pef_vec -DHAVE_pef_xlib_vec -DHAVE_sym_vec")

set(bfd_srcs
	archive.c
	archures.c
	bfd.c
	bfdio.c
	bfdwin.c
	cache.c
	coffgen.c
	corefile.c
	format.c
	init.c
	libbfd.c
	opncls.c
	reloc.c
	section.c
	syms.c
	targets.c
	hash.c
	linker.c
	srec.c
	binary.c
	tekhex.c
	ihex.c
	stabs.c
	stab-syms.c
	merge.c
	dwarf2.c
	simple.c
	archive64.c
		
	mach-o.c
	pef.c
	xsym.c
	cpu-i386.c
	cpu-powerpc.c
	cpu-rs6000.c
)

set_source_files_properties(archures.c targets.c PROPERTIES COMPILE_FLAGS "${extra_arch_defs}")

add_library(bfd OBJECT ${bfd_srcs})

