SUBDIRS = icons

desktopdir = $(datadir)/applications
desktop_in_files = mate-tweak.desktop.in
desktop_DATA = $(desktop_in_files:.desktop.in=.desktop)

$(desktop_DATA): $(desktop_in_files)
	$(AM_V_GEN) $(MSGFMT) --desktop --keyword= --keyword=Name --keyword=Comment --keyword=Keywords --template $< -d $(top_srcdir)/po -o $@

#data_files = [
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-xrender.desktop',]),
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-glx.desktop',]),
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-xr_glx_hybrid.desktop',]),
#    ('{prefix}/share/applications'.format(prefix=sys.prefix), ['data/marco-no-composite.desktop',]),
#    ('{prefix}/share/polkit-1/actions'.format(prefix=sys.prefix), ['data/org.mate.mate-tweak.policy',]),
#    ('{prefix}/lib/mate-tweak'.format(prefix=sys.prefix), ['data/mate-tweak.ui', 'util/mate-tweak-helper']),
#]

man_MANS = mate-tweak.1

pkgdata_DATA = mate-tweak.ui

CLEANFILES = $(desktop_DATA)

EXTRA_DIST = \
	meson.build \
	$(pkgdata_DATA) \
	$(man_MANS)

install-data-hook: $(UPDATE_DESKTOP)

uninstall-hook: $(UPDATE_DESKTOP)

