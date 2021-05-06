load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library", "cc_import")

cc_import(
    name = "common_header",
    hdrs = [ "common.h"]
)

cc_library(
    name = "vm",
    srcs = glob(["*.c"], exclude=["main.c"]),
    hdrs = glob(["*.h"], exclude=["common.h"]),
    deps = [
         ":common_header",
    ]
)

cc_binary(
    name = "main",
    srcs = ["main.c"],
    deps = [
        ":common_header",
        ":vm",
    ],
)
