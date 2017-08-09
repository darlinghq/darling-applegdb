add_definitions(
	-DHAVE_CONFIG_H
	-DRL_LIBRARY_VERSION="4.3"
)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}
	${CMAKE_CURRENT_SOURCE_DIR}/..
)

set(readline_srcs
	readline.c
	funmap.c
	keymaps.c
	vi_mode.c
	parens.c
	rltty.c
	complete.c
	bind.c
	isearch.c
	display.c
	signals.c
	# emacs_keymap.c
	# vi_keymap.c
	util.c
	kill.c
	undo.c
	macro.c
	input.c
	callback.c
	terminal.c
	# xmalloc.c
	history.c
	histsearch.c
	histexpand.c
	histfile.c
	nls.c
	search.c
	shell.c
	# savestring.c
	tilde.c
	text.c
	misc.c
	compat.c
	mbutil.c
	support/wcwidth.c
)

add_library(libreadline OBJECT ${readline_srcs})

