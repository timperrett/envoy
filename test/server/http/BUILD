package(default_visibility = ["//visibility:public"])

load("//bazel:envoy_build_system.bzl", "envoy_cc_test")

envoy_cc_test(
    name = "admin_test",
    srcs = ["admin_test.cc"],
    deps = [
        "//source/common/http:message_lib",
        "//source/common/profiler:profiler_lib",
        "//source/server/http:admin_lib",
        "//test/mocks/server:server_mocks",
        "//test/test_common:environment_lib",
        "//test/test_common:utility_lib",
    ],
)

envoy_cc_test(
    name = "health_check_test",
    srcs = ["health_check_test.cc"],
    deps = [
        "//source/common/buffer:buffer_lib",
        "//source/server/http:health_check_lib",
        "//test/mocks/server:server_mocks",
        "//test/test_common:utility_lib",
    ],
)
