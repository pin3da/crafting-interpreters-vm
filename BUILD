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
    name = "value",
    srcs = ["value.c"],
    hdrs = ["value.h"],
    deps = [
         ":common_header",
         ":memory",
    ]
)

cc_library(
    name = "debug",
    srcs = ["debug.c"],
    hdrs = ["debug.h"],
    deps = [
         ":common_header",
         ":chunk",
    ]
)

cc_library(
    name = "chunk",
    srcs = ["chunk.c"],
    hdrs = ["chunk.h"],
    deps = [
        ":common_header",
        ":memory",
        ":value",
    ]
)

cc_library(
    name = "vm",
    srcs = ["vm.c"],
    hdrs = ["vm.h"],
    deps = [
        ":common_header",
        ":memory",
        ":value",
        ":chunk",
        ":debug",
    ]
)

cc_binary(
    name = "main",
    srcs = ["main.c"],
    deps = [
        ":common_header",
        ":chunk",
        ":debug",
        ":memory",
        ":vm",
    ],
)
