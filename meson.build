project(
    'mesontestDlangModule',
    'd',
    license: 'GPL-3.0-or-later',
    meson_version: '>=0.50',
    version: '0.0.1',
)

conf = configuration_data()

source = configure_file(
  input: 'source/app.d',
  output: 'app.d',
  configuration: conf,
)

dlang = import('dlang')

dlang.generate_dub_file(meson.project_name().to_lower(), meson.source_root(),
                        authors: 'Rasmus Thomsen',
                        description: 'Test executable',
                        copyright: 'Copyright © 2019, Rasmus Thomsen',
                        license: 'GPL-3.0',
                        sourceFiles: source,
                        targetType: 'executable',
)
