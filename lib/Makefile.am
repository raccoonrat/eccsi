#ECCSIDIR = @ECCSIDIR@
#EVDIR = @EVDIR@
AUTOMAKE_OPTIONS = std-options subdir-objects

lib_LTLIBRARIES= libesdata.la libesprng.la libescrypt.la

libesdata_la_SOURCES = msdb/msdb.c
libesdata_la_CFLAGS = -I$(top_srcdir)/include -I${ECCSIDIR}/include 
libesdata_la_LIBADD = -lm -lrt -lpthread -ldl
libesdata_la_LDFLAGS = -version-info 1:0:1

libesprng_la_SOURCES = esprng/esprng.c
libesprng_la_CFLAGS = -I$(top_srcdir)/include -I${ECCSIDIR}/include 
libesprng_la_LIBADD = -lm -lrt -lpthread -ldl
libesprng_la_LDFLAGS = -version-info 1:0:1

libescrypt_la_SOURCES = utils/utils.c data/userParameters.c data/communityParameters.c data/mikeySakkeParameters.c sakke/sakke.c  eccsi/eccsi.c
libescrypt_la_CFLAGS = -I$(top_srcdir)/include -I${ECCSIDIR}/include -I${ECCSIDIR}/utils -I${ECCSIDIR}/data  -I${ECCSIDIR}/sakke -I${ECCSIDIR}/eccsi
libescrypt_la_LIBADD = -lm -lrt -lpthread -ldl -L/usr/lib/x86_64-linux-gnu -lssl -lcrypto libesdata.la libesprng.la
libescrypt_la_LDFLAGS = -version-info 1:0:1
