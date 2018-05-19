ACLOCAL_AMFLAGS = -I m4

if MPI
AM_DISTCHECK_CONFIGURE_FLAGS = --enable-mpi
endif

SUBDIRS = UTIL SRC . TESTS EXAMPLES PARPACK

EXTRA_DIST = README PARPACK_CHANGES CHANGES DOCUMENTS VISUAL_STUDIO \
detect_arpack_bug.m4 CMakeLists.txt

pkgconfig_DATA = arpack@LIBSUFFIX@.pc

DISTCLEANFILES = $(pkgconfig_DATA)

rs_autoconf_hack:
	@mkdir -p rs-hack-output
	@echo $(rs_hack_f77_mangled_normal) > rs-hack-output/mangled-normal
	@echo $(rs_hack_f77_mangled_underscore) > rs-hack-output/mangled-underscore
