
load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library", "cc_import")

cc_import(
    name = "common_header",
    hdrs = [ "common.h"]
)

cc_library(
    name = "memory",
    srcs = ["memory.c"],
    hdrs = ["memory.h"],
    deps = [":common_header"]
)

cc_library(
    name = "chunk",
    srcs = ["chunk.c"],
    hdrs = ["chunk.h"],
    deps = [
        ":common_header",
        ":memory"
    ]
)

cc_binary(
    name = "main",
    srcs = ["main.c"],
    deps = [
        ":common_header",
        ":chunk",
    ]
)
