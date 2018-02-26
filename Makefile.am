AM_MAKEFLAGS = --no-print-directory
ACLOCAL_AMFLAGS = -I build-aux

AM_CFLAGS = $(WARNING_CFLAGS) $(BUILD_CFLAGS) $(MISC_CFLAGS)
AM_LDFLAGS = $(BUILD_LDFLAGS)

#SUBDIRS = src
dist_doc_DATA = README

include_HEADERS = src/knot_types.h src/knot_protocol.h
pkginclude_HEADERS = src/knot_types.h src/knot_protocol.h

libjson_cincludedir = $(includedir)/knotprotocol

lib_LTLIBRARIES = libknotprotocol.la
libknotprotocol_la_SOURCES = $(linux_headers) $(pkg_include_HEADERS) src/knot_protocol.c

pkgconfigdir = $(libdir)/pkgconfig

pkgconfig_DATA = src/knotprotocol.pc

MAINTAINERCLEANFILES = Makefile.in \
	aclocal.m4 configure config.h.in config.sub config.guess \
	ltmain.sh depcomp compile missing install-sh
