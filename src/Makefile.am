# This is _NOT_ the library release version, it's an API version.
# Please read Chapter 6 "Library interface versions" of the libtool documentation before making any modification
LIBVERSION=0:0:0

INCLUDES = $(all_includes) -I$(top_srcdir)/include
AM_CFLAGS = ${CFLAGS} -fPIC ${SYMBOL_VISIBILITY}

lib_LTLIBRARIES = librtlsdr.la

librtlsdr_la_SOURCES = librtlsdr.c tuner_e4k.c tuner_fc0012.c tuner_fc0013.c tuner_fc2580.c tuner_r820t.c
librtlsdr_la_LDFLAGS = -version-info $(LIBVERSION)

bin_PROGRAMS         = rtl_433

rtl_433_SOURCES      = rtl_433.c
rtl_433_LDADD        = librtlsdr.la $(LIBM)
