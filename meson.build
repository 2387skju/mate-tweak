project('mate-tweak',
  version : '22.10.0',
  meson_version: '>= 0.47.0'
  )

i18n = import('i18n')
python = import('python')
py3 = find_program('python3', required:true)

#just copyed from mozo, delete/edit this: dependency('libmate-menu', version: '>= 1.21.0')
#just copyed from mozo, delete/edit this: dependency('pygobject-3.0')

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
#some var's are just copy from mate-control-center-master
#bindir = join_paths(prefix, get_option('bindir'))
#sbindir = join_paths(prefix, get_option('sbindir'))
libexecdir = join_paths(prefix, get_option('libexecdir'))
libdir = join_paths(prefix, get_option('libdir'))
localedir = join_paths(prefix, get_option('localedir'))
#mandir = join_paths(prefix, get_option('mandir'))
#sysconfdir = join_paths(prefix, get_option('sysconfdir'))

#some var's are just copy from mate-control-center-master
#pkgdatadir = join_paths(datadir, meson.project_name())
#pixmaps = join_paths(pkgdatadir, 'pixmaps')
#background = join_paths(datadir, 'backgrounds')
#wallpaperdir = join_paths(datadir, 'mate-background-properties')
#desktopdir = join_paths(datadir, 'applications')
#icondir = join_paths(datadir, 'icons')
#schemadir = join_paths (datadir, 'glib-2.0', 'schemas')
policydir = join_paths (datadir, 'polkit-1', 'actions')
#timezonedir = join_paths (datadir, 'mate-time-admin', 'map')
#directorydir = join_paths(datadir, 'desktop-directories')
#mime = join_paths(datadir, 'mime', 'packages')
#gettext = meson.project_name() + '-2.0'

mate_tweak_in = configuration_data()
mate_tweak_in.set('PYTHON', py3.path())
mate_tweak_in.set('PYOPTIONS', '-OOt')

mate_tweak = configure_file(input: 'mate-tweak',
  output: 'mate-tweak',
  configuration: mate_tweak_in,
  )

install_data(mate_tweak,
  install_mode: 'rwxr-xr-x',
  install_dir: get_option('bindir')
  )
install_data(['marco-compton','marco-glx','marco-no-composite','marco-picom','marco-xrender','marco-xr_glx_hybrid'],
  install_mode: 'rwxr-xr-x',
  install_dir: get_option('bindir')
  )

subdir('po')
subdir('MateTweak')
subdir('data')

meson.add_install_script('post_install.py')
