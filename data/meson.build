

desktop_in = configuration_data()
desktop_in.set('VERSION', meson.project_version())

desktop_file = 'mate-tweak.desktop'
i18n.merge_file(
  input: configure_file(
    input: desktop_file + '.in.in',
    output: desktop_file + '.in',
    configuration : desktop_in,
    ),
  output: desktop_file,
  po_dir: join_paths(meson.source_root(), 'po'),
  type: 'desktop',
  install: true,
  install_dir : join_paths(datadir, 'applications')
  )

desktop_file = 'marco-xrender.desktop'
i18n.merge_file(
  input: configure_file(
    input: desktop_file + '.in.in',
    output: desktop_file + '.in',
    configuration : desktop_in,
    ),
  output: desktop_file,
  po_dir: join_paths(meson.source_root(), 'po'),
  type: 'desktop',
  install: true,
  install_dir : join_paths(datadir, 'applications')
  )

desktop_file = 'marco-glx.desktop'
i18n.merge_file(
  input: configure_file(
    input: desktop_file + '.in.in',
    output: desktop_file + '.in',
    configuration : desktop_in,
    ),
  output: desktop_file,
  po_dir: join_paths(meson.source_root(), 'po'),
  type: 'desktop',
  install: true,
  install_dir : join_paths(datadir, 'applications')
  )

desktop_file = 'marco-xr_glx_hybrid.desktop'
i18n.merge_file(
  input: configure_file(
    input: desktop_file + '.in.in',
    output: desktop_file + '.in',
    configuration : desktop_in,
    ),
  output: desktop_file,
  po_dir: join_paths(meson.source_root(), 'po'),
  type: 'desktop',
  install: true,
  install_dir : join_paths(datadir, 'applications')
  )

desktop_file = 'marco-no-composite.desktop'
i18n.merge_file(
  input: configure_file(
    input: desktop_file + '.in.in',
    output: desktop_file + '.in',
    configuration : desktop_in,
    ),
  output: desktop_file,
  po_dir: join_paths(meson.source_root(), 'po'),
  type: 'desktop',
  install: true,
  install_dir : join_paths(datadir, 'applications')
  )

install_data('org.mate.mate-tweak.policy',
    install_dir: '/usr/share/polkit-1/actions/'
    #install_dir: '/app/share/polkit-1/actions/'
    #install_dir: '/etc/polkit-1/localauthority/50-local.d/'
)

install_man('mate-tweak.1')
install_data('mate-tweak.ui',
    install_dir: join_paths('/usr/lib/', meson.project_name())
)

