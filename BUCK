include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'coroutine',
  header_namespace = 'boost/coroutine',
  exported_headers = subdir_glob([
    ('include/boost/coroutine', '**/*.hpp'),
  ]),
  srcs = glob([
    'src/detail/**/*.cpp',
    'src/*.cpp',
  ]),
  platform_srcs = [
    ('^macos.*', glob(['src/posix/**/*.cpp'])),
    ('^linux.*', glob(['src/posix/**/*.cpp'])),
    ('^windows.*', glob(['src/windows/**/*.cpp'])),
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
