bin_PROGRAMS = estclient_simple
estclient_simple_includedir=$(includedir)/est
estclient_simple_SOURCES = estclient-simple.c ../util/utils.c 
AM_CFLAGS = -I../.. -I$(srcdir)/../../src/est

if FREEBSD 
DL=
else
DL=-ldl
endif

LIBEST_COREDIR = ../../src/est
SUBDIRS = $(LIBEST_COREDIR)
estclient_simple_LDFLAGS = -L$(LIBEST_COREDIR)/.libs -lest
estclient_simple_DEPENDENCIES = $(LIBEST_COREDIR)/.libs/libest.*
