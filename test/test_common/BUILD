package(default_visibility = ["//visibility:public"])

load("//bazel:envoy_build_system.bzl", "envoy_cc_library", "envoy_cc_test_library")

cc_library(
    name = "printers_includes",
    hdrs = ["printers.h"],
)

envoy_cc_test_library(
    name = "environment_lib",
    srcs = ["environment.cc"],
    hdrs = ["environment.h"],
    deps = [
        "//include/envoy/server:options_interface",
        "//source/common/common:assert_lib",
        "//source/common/json:json_loader_lib",
        "//source/server:options_lib",
    ],
)

envoy_cc_test_library(
    name = "network_utility_lib",
    srcs = ["network_utility.cc"],
    hdrs = ["network_utility.h"],
    deps = [
        ":utility_lib",
        "//source/common/common:assert_lib",
        "//source/common/network:address_lib",
        "//source/common/network:utility_lib",
        "//source/common/runtime:runtime_lib",
    ],
)

envoy_cc_library(
    name = "printers_lib",
    srcs = ["printers.cc"],
    deps = [
        ":printers_includes",
        "//source/common/buffer:buffer_lib",
        "//source/common/http:header_map_lib",
        "//source/common/redis:codec_lib",
    ],
)

envoy_cc_test_library(
    name = "utility_lib",
    srcs = ["utility.cc"],
    hdrs = ["utility.h"],
    deps = [
        "//include/envoy/buffer:buffer_interface",
        "//include/envoy/network:address_interface",
        "//source/common/common:empty_string",
        "//source/common/http:header_map_lib",
        "//source/common/network:address_lib",
    ],
)
