load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["docs-no-retest.go"],
    importpath = "k8s.io/test-infra/prow/plugins/docs-no-retest",
    visibility = ["//visibility:public"],
    deps = [
        "//prow/github:go_default_library",
        "//prow/plugins:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["docs-no-retest_test.go"],
    embed = [":go_default_library"],
    importpath = "k8s.io/test-infra/prow/plugins/docs-no-retest",
    deps = [
        "//prow/github:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
