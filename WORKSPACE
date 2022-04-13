workspace(
    name = "rules_nodejs_playground",
)

load("//tools:bazel_deps.bzl", "fetch_dependencies")

fetch_dependencies()

load("@build_bazel_rules_nodejs//:repositories.bzl", "build_bazel_rules_nodejs_dependencies")

build_bazel_rules_nodejs_dependencies()

load("@build_bazel_rules_nodejs//:index.bzl", "node_repositories", "npm_install")

node_repositories(
    node_urls = ["https://nodejs.org/dist/v{version}/{filename}"],
    node_version = "16.5.0",
)

npm_install(
    name = "npm",
    # exports_directories_only =  False,
    package_json = "//:package.json",
    package_lock_json = "//:package-lock.json",
    strict_visibility = False,
)
