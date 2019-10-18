package(default_visibility = ["//:__subpackages__"])

load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kt_android_library")

kt_android_library(
    name = "oxygen",
    srcs = glob(["src/main/java/**/*.java", "src/main/java/**/*.kt"]),
    deps = [
        "@maven//androidx/annotation:annotation",
        "@maven//com/google/code/findbugs:jsr305",
        "@maven//io/reactivex/rxjava2:rxjava",
        "@maven//org/jetbrains:annotations",
    ],
)