load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "bart",
    srcs = [
        "dispatcher.go",
        "email.go",
        "encoding.go",
        "mimeparts.go",
        "yaml_reader.go",
    ],
    importpath = "github.com/mp4096/m/src/cmd/bart",
    visibility = ["//visibility:private"],
    deps = [
        "@com_github_cbroglie_mustache//:go_default_library",
        "@com_github_hashicorp_go_multierror//:go_default_library",
        "@com_github_howeyc_gopass//:go_default_library",
        "@com_github_jaytaylor_html2text//:go_default_library",
        "@in_gopkg_yaml_v2//:go_default_library",
    ],
)

go_binary(
    name = "run",
    srcs = ["main.go"],
    visibility = ["//visibility:public"],
    deps = [":bart"],
)
