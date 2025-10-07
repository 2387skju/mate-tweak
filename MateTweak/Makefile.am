## Process this file with automake to produce Makefile.in
appdir = $(pythondir)/MateTweak
app_PYTHON = __init__.py MainWindow.py
nodist_app_PYTHON = config.py

config.py: config.py.in
	$(AM_V_GEN)sed					\
		-e s!\@prefix\@!$(prefix)!		\
		-e s!\@datadir\@!$(datadir)!		\
		-e s!\@pkgdatadir\@!$(pkgdatadir)!	\
		-e s!\@PACKAGE\@!$(PACKAGE)!		\
		-e s!\@VERSION\@!$(VERSION)!		\
		-e s!\@GETTEXT_PACKAGE\@!$(GETTEXT_PACKAGE)!	\
		-e s!\@libexecdir\@!$(libexecdir)!	\
		-e s!\@localedir\@!$(localedir)!	\
		-e s!\@sysconfdir\@!$(sysconfdir)!	\
		< $< > $@
config.py: Makefile

CLEANFILES = config.py
EXTRA_DIST = \
	config.py.in \
	meson.build

#just copied from mozo, delete/edit this:
all-local: config.py

