package(default_visibility = ["//visibility:public"])

load("@my_deps//:requirements.bzl", "requirement")

py_library(
    name = "__init__",
    srcs = ["__init__.py"],
)

py_library(
    name = "deploy",
    srcs = ["deploy.py"],
    deps = [
        "//clarify/serve/utils:deployment_utils",
        "//clarify/utils:fs_utils",
        requirement("tensorflow"),
    ],
)

py_test(
    name = "deploy_test",
    srcs = ["deploy_test.py"],
    deps = [
        "//clarify/serve/label_state/gcf:deploy",
        "//clarify/utils:cfg_utils",
    ],
)

py_library(
    name = "main",
    srcs = ["main.py"],
    deps = [
        "//clarify/serve/utils:deployment_utils",
        "//clarify/utils:fs_utils",
        requirement("tensorflow"),
        requirement("numpy"),
        requirement("scikit-learn"),
        requirement("google-cloud-firestore"),
    ],
)

py_test(
    name = "main_test",
    srcs = ["main_test.py"],
    deps = [
        "//clarify/serve/label_state/gcf:main",
        requirement("mock"),
        requirement("numpy"),
    ],
)
