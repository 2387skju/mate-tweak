SUBDIRS = icons

desktopdir = $(datadir)/applications
desktop_in_files = mate-tweak.desktop.in
desktop_DATA = $(desktop_in_files:.desktop.in=.desktop)

$(desktop_DATA): $(desktop_in_files)
	$(AM_V_GEN) $(MSGFMT) --desktop --keyword= --keyword=Name --keyword=Comment --keyword=Keywords --template $< -d $(top_srcdir)/po -o $@

#origin:
#data_files = [
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-xrender.desktop',]),
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-glx.desktop',]),
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-xr_glx_hybrid.desktop',]),
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-no-composite.desktop',]),
#    ('{prefix}/share/polkit-1/actions'.format(prefix=sys.prefix), ['data/org.mate.mate-tweak.policy',]),
#    ('{prefix}/lib/mate-tweak'.format(prefix=sys.prefix), ['data/mate-tweak.ui', 'util/mate-tweak-helper']),
#]

#just copied from mozo, delete/edit this:
##appdir = $(pythondir)/MateTweak
#just copied from mozo, delete/edit this:
##app_PYTHON = __init__.py
nodist_app_PYTHON = org.mate.mate-tweak.policy

org.mate.mate-tweak.policy: org.mate.mate-tweak.policy.in
	$(AM_V_GEN)sed					\
		-e s!\@prefix\@!$(prefix)!		\
		-e s!\@datadir\@!$(datadir)!		\
		-e s!\@localedir\@!$(localedir)!	\
		-e s!\@pkgdatadir\@!$(pkgdatadir)!	\
		-e s!\@PACKAGE\@!$(PACKAGE)!		\
		-e s!\@VERSION\@!$(VERSION)!		\
		-e s!\@GETTEXT_PACKAGE\@!$(GETTEXT_PACKAGE)!	\
		-e s!\@libexecdir\@!$(libexecdir)!	\
		-e s!\@libdir\@!$(libdir)!	\
		-e s!\@sysconfdir\@!$(sysconfdir)!	\
		< $< > $@
org.mate.mate-tweak.policy: Makefile

#just copied from mozo, delete/edit this: all-local: org.mate.mate-tweak.policy



man_MANS = mate-tweak.1

pkgdata_DATA = mate-tweak.ui

CLEANFILES = $(desktop_DATA)  org.mate.mate-tweak.policy

EXTRA_DIST = \
	org.mate.mate-tweak.policy.in \
	meson.build \
	$(pkgdata_DATA) \
	$(man_MANS)

#just copied from mozo, delete/edit this:
install-data-hook: $(UPDATE_DESKTOP)

#just copied from mozo, delete/edit this:
uninstall-hook: $(UPDATE_DESKTOP)

