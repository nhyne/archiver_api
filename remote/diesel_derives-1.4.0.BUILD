"""
cargo-raze crate build file.

DO NOT EDIT! Replaced on runs of cargo-raze
"""
package(default_visibility = [
  # Public for visibility by "@raze__crate__version//" targets.
  #
  # Prefer access through "//cargo", which limits external
  # visibility to explicit Cargo.toml dependencies.
  "//visibility:public",
])

licenses([
  "restricted", # "MIT OR Apache-2.0"
])

load(
    "@io_bazel_rules_rust//rust:rust.bzl",
    "rust_library",
    "rust_binary",
    "rust_test",
)



rust_library(
    name = "diesel_derives",
    crate_root = "src/lib.rs",
    crate_type = "proc-macro",
    edition = "2015",
    srcs = glob(["**/*.rs"]),
    deps = [
        "@raze__proc_macro2__0_4_30//:proc_macro2",
        "@raze__quote__0_6_13//:quote",
        "@raze__syn__0_15_43//:syn",
    ],
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "1.4.0",
    crate_features = [
        "default",
        "postgres",
    ],
)

# Unsupported target "tests" with type "test" omitted
