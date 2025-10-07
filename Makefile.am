## Process this file with automake to produce Makefile.in

appdir = $(pythondir)/MateTweak

SUBDIRS = po data MateTweak

CLEANFILES=

bin_SCRIPTS = mate-tweak
CLEANFILES += mate-tweak

DISTCLEANFILES = ChangeLog

DISTCHECK_CONFIGURE_FLAGS = \
	--disable-icon-update \
	CFLAGS='-Wno-deprecated-declarations'

mate-tweak: mate-tweak.in
	$(AM_V_GEN)sed -e s!\@PYTHON\@!@PYTHON@!	\
	    -e s!\@PYOPTIONS\@!-OOt!			\
	    -e s!\@appdir\@!$@appdir@!			\
	    < $< > $@
mate-tweak: Makefile

EXTRA_DIST = \
	autogen.sh \
	meson.build \
	mate-tweak.in \
	post_install.py \
	po/meson.build

# Build ChangeLog from GIT  history
ChangeLog:
	$(AM_V_GEN) if test -d $(top_srcdir)/.git; then \
		GIT_DIR="$(top_srcdir)/.git" git log --stat > $@; \
	fi

dist: ChangeLog

.PHONY: ChangeLog
