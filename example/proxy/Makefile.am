bin_PROGRAMS = estproxy
estproxy_SOURCES = estproxy.c ../util/utils.c ../util/simple_server.c 
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
estproxy_LDFLAGS = -L$(LIBEST_COREDIR)/.libs -lest
estproxy_DEPENDENCIES = $(LIBEST_COREDIR)/.libs/libest.*

EXTRA_DIST = createRA.sh runproxy.sh estExampleCA.cnf
