SUBDIRS = data

AM_CFLAGS = $(CHAFA_CFLAGS) $(GLIB_CFLAGS)
LDADD = $(GLIB_LIBS) $(top_builddir)/chafa/libchafa.la

## --- Backend tests ---

noinst_PROGRAMS = \
	term-info-test

term_info_test_SOURCES = \
	term-info-test.c

## --- Frontend tests ---

TOOL_CHECKS = \
	chafa-tool-bad-test.sh \
	chafa-tool-cmode-test.sh \
	chafa-tool-format-test.sh \
	chafa-tool-loader-test.sh \
	chafa-tool-options-test.sh \
	chafa-tool-pipe-test.sh

TESTS = \
	term-info-test \
	$(TOOL_CHECKS)

AM_TESTS_ENVIRONMENT = \
	export top_builddir=$(top_builddir) \
	export top_srcdir=$(top_srcdir) \
	;

## --- General ---

## Include $(top_builddir)/chafa to get generated chafaconfig.h.

AM_CPPFLAGS = \
	-I$(top_srcdir)/chafa \
	-I$(top_builddir)/chafa

EXTRA_DIST = \
	$(TOOL_CHECKS) \
	chafa-tool-gallery.sh \
	chafa-tool-test-common.sh
