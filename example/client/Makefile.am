bin_PROGRAMS = estclient
estclient_includedir=$(includedir)/est
estclient_SOURCES = estclient.c ../util/utils.c 
AM_CFLAGS = -I../.. -I$(srcdir)/../../src/est

if FREEBSD 
DL=
else
DL=-ldl
endif

if DISABLE_PTHREAD
PTHREAD=
else
PTHREAD=-lpthread
endif

LIBEST_COREDIR = ../../src/est
SUBDIRS = $(LIBEST_COREDIR)
estclient_LDFLAGS = -L$(LIBEST_COREDIR)/.libs -lest
estclient_DEPENDENCIES = $(LIBEST_COREDIR)/.libs/libest.*
