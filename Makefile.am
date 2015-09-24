AUTOMAKE_OPTIONS = foreign nostdinc subdir-objects

ACLOCAL_AMFLAGS = -I .

lib_LTLIBRARIES = libbrotli.la

CSOURCES = brotli/dec/bit_reader.c brotli/dec/decode.c		\
  brotli/dec/huffman.c brotli/dec/state.c brotli/dec/streams.c

HHEADERS = 

EXTRA_DIST = AUTHORS README

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libbrotli.pc
pkgincludedir= $(includedir)/brotli
pkginclude_HEADERS = brotli/dec/decode.h brotli/dec/state.h	\
 brotli/dec/streams.h brotli/dec/types.h

LIBBROTLI_VERSION_INFO = -version-info 1:0:0
# This flag accepts an argument of the form current[:revision[:age]]. So,
# passing -version-info 3:12:1 sets current to 3, revision to 12, and age to
# 1.
#
# If either revision or age are omitted, they default to 0. Also note that age
# must be less than or equal to the current interface number.
#
# Here are a set of rules to help you update your library version information: 
#
# 1.Start with version information of 0:0:0 for each libtool library.
#
# 2.Update the version information only immediately before a public release of
# your software. More frequent updates are unnecessary, and only guarantee
# that the current interface number gets larger faster.
#
# 3.If the library source code has changed at all since the last update, then
# increment revision (c:r+1:a)
#
# 4.If any interfaces have been added, removed, or changed since the last
# update, increment current, and set revision to 0. (c+1:r=0:a)
#
# 5.If any interfaces have been added since the last public release, then
# increment age. (c:r:a+1)
#
# 6.If any interfaces have been removed since the last public release, then
# set age to 0. (c:r:a=0)
#

AM_LDFLAGS =

libbrotli_la_LDFLAGS_EXTRA =

libbrotli_la_LDFLAGS = $(AM_LDFLAGS) $(libbrotli_la_LDFLAGS_EXTRA)

libbrotli_la_CFLAGS_EXTRA =

libbrotli_la_CPPFLAGS_EXTRA = -DBROTLI_BUILDING_LIBRARY

libbrotli_la_CFLAGS = $(AM_CFLAGS) $(libbrotli_la_CFLAGS_EXTRA)
libbrotli_la_CPPFLAGS = $(AM_CPPFLAGS) $(libbrotli_la_CPPFLAGS_EXTRA)
libbrotli_la_SOURCES = $(CSOURCES) $(HHEADERS)

# where to install the c-ares headers
libbrotli_ladir = $(includedir)

brotli:
	echo "Install symlink 'brotli' to brotli source code root"
	exit 1