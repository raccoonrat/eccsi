AUTOMAKE_OPTIONS = foreign
CFLAGS= @CFLAGS@ -I$(top_srcdir)/include -I${ECCSIDIR}/include  -I${EVDIR}/include -I${ECCSIDIR}/lib/utils -I${ECCSIDIR}/lib/sakke -I${ECCSIDIR}/lib/eccsi -I${ECCSIDIR}/lib/data -DDEBUG -g
#CFLAGS= @CFLAGS@ -I$(top_srcdir)/include -I${ECCSIDIR}/include  -I${EVDIR}/include
#bin_PROGRAMS = dhsvr_ondmand dhclt tuxztca_svr tuxztca_clt es_demo_1 es_demo_2
bin_PROGRAMS = es_demo_1 es_demo_2 

#dhsvr_ondmand_SOURCES = dhsvr_ondmand.c
#dhsvr_ondmand_CFLAGS = ${CFLAGS}
#dhsvr_ondmand_LDADD = ../lib/libtux_ztdh.la
#
#tuxztca_svr_SOURCES = tuxztca_svr.c
#tuxztca_svr_CFLAGS  = ${CFLAGS}
#tuxztca_svr_LDADD   = ../lib/libtux_ztdh.la
#

es_demo_1_SOURCES = es_demo_1.c 
es_demo_1_CFLAGS = ${CFLAGS}
#es_demo_1_LDADD = ../lib/libtux_ztdh.la -levent -lpthread
es_demo_1_LDADD = -L/usr/lib/x86_64-linux-gnu  -lssl -lcrypto \
	../lib/libesprng.la ../lib/libesdata.la ../lib/libescrypt.la

es_demo_2_SOURCES = es_demo_2.c
es_demo_2_CFLAGS = ${CFLAGS}
#es_demo_2_LDADD = ../lib/libtux_ztdh.la -levent -lpthread
es_demo_2_LDADD = -L/usr/lib/x86_64-linux-gnu  -lssl -lcrypto \
	../lib/libesprng.la ../lib/libesdata.la ../lib/libescrypt.la

