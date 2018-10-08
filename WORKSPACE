workspace(name = "com_github_Xjs_bazel_go_pack_demo")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.15.4/rules_go-0.15.4.tar.gz"],
    sha256 = "7519e9e1c716ae3c05bd2d984a42c3b02e690c5df728dc0a84b23f90c355c5a1",
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "d9cb7e3cbaea8efd7bd1c9e27d6aaed335acfbd27e4590bb344baa35032ec612",
    strip_prefix = "bazel-gazelle-0.14.0",
    url = "https://github.com/bazelbuild/bazel-gazelle/archive/0.14.0.zip",
)

load("@io_bazel_rules_go//go:def.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()

go_register_toolchains()

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()

go_repository(
    name = "org_gonum_v1_gonum",
    importpath = "gonum.org/v1/gonum",
    sha256 = "509ddae2d42ac323ba4afcfd82cf47205b8dee1e51b203ebfa31561d1507fd70",
    strip_prefix = "gonum-e9e56344e335b77c52738092530a60fd12db0351",
    urls = ["https://github.com/gonum/gonum/archive/e9e56344e335b77c52738092530a60fd12db0351.zip"],
)
