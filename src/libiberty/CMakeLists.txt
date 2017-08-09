project(libiberty)

add_definitions(-DHAVE_CONFIG_H)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}
	${CMAKE_CURRENT_SOURCE_DIR}/../include
)

set(iberty_srcs
	cplus-dem.c
	cp-demangle.c
	md5.c
	alloca.c
	argv.c
	choose-temp.c
	concat.c
	cp-demint.c
	dyn-string.c
	fdmatch.c
	fibheap.c
	floatformat.c
	fnmatch.c
	fopen_unlocked.c
	getopt.c
	getopt1.c
	getpwd.c
	getruntime.c
	hashtab.c
	hex.c
	lbasename.c
	lrealpath.c
	make-relative-prefix.c
	make-temp-file.c
	objalloc.c
	obstack.c
	partition.c
	pexecute.c
	physmem.c
	pex-common.c
	pex-one.c
	pex-unix.c
	safe-ctype.c
	sort.c
	spaces.c
	splay-tree.c
	strerror.c
	strsignal.c
	ternary.c
	unlink-if-ordinary.c
	xatexit.c
	xexit.c
	# xmalloc.c
	xmemdup.c
	xstrdup.c
	xstrerror.c
	xstrndup.c

	mempcpy.c
	strverscmp.c
)

add_library(libiberty OBJECT ${iberty_srcs})

