cc_library(
    name = 'lxdialog',
    srcs = glob(['lxdialog/*.c']),
    hdrs = glob(['lxdialog/*.h']),
)

cc_library(
    name = 'zconf',
    srcs = ['zconf.tab.c'],
    hdrs = [
        'lkc.h',
        'expr.h',
        'list.h',
        'lkc_proto.h',
    ],
    textual_hdrs = [
        'confdata.c',
        'expr.c',
        'menu.c',
        'symbol.c',
        'util.c',
        'zconf.hash.c',
        'zconf.lex.c',
    ],
)

cc_binary(
    name = 'conf',
    srcs = ['conf.c'],
    deps = [':zconf'],
)

cc_binary(
    name = 'mconf',
    srcs = ['mconf.c'],
    deps = [':zconf', ':lxdialog'],
)
