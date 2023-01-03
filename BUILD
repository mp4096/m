load("@bazel_gazelle//:def.bzl", "gazelle")
load("@io_bazel_rules_go//go:def.bzl", "nogo")

# gazelle:prefix github.com/mp4096/m
gazelle(name = "gazelle")

nogo(
    name = "nogo",
    vet = True,
    config = "nogo_config.json",
    visibility = ["//visibility:public"],
)
