add_definitions(
	-DLOCALEDIR="/usr/share/locale"
	-DGNULOCALEDIR="/usr/share/locale"
	-DLOCALE_ALIAS_PATH="/usr/share/locale"
	-DHAVE_CONFIG_H
)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

set(libintl_srcs
	intl-compat.c
	bindtextdom.c
	dcgettext.c
	dgettext.c
	gettext.c
	finddomain.c
	loadmsgcat.c
	localealias.c
	textdomain.c
	l10nflist.c
	explodename.c
)

add_library(libintl OBJECT ${libintl_srcs})

