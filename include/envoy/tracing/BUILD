package(default_visibility = ["//visibility:public"])

load("//bazel:envoy_build_system.bzl", "envoy_cc_library")

envoy_cc_library(
    name = "context_interface",
    hdrs = ["context.h"],
)

envoy_cc_library(
    name = "http_tracer_interface",
    hdrs = ["http_tracer.h"],
    deps = [
        "//include/envoy/http:access_log_interface",
        "//include/envoy/http:header_map_interface",
    ],
)
