# Kotlin Rule
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

rules_kotlin_version = "legacy-modded-1_0_0-01"
rules_kotlin_sha = "b7984b28e0a1e010e225a3ecdf0f49588b7b9365640af783bd01256585cbb3ae"
http_archive(
    name = "io_bazel_rules_kotlin",
    urls = ["https://github.com/bazelbuild/rules_kotlin/archive/%s.zip" % rules_kotlin_version],
    type = "zip",
    strip_prefix = "rules_kotlin-%s" % rules_kotlin_version,
    sha256 = rules_kotlin_sha,
)

load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kotlin_repositories", "kt_register_toolchains")
kotlin_repositories() # if you want the default. Otherwise see custom kotlinc distribution below
kt_register_toolchains() # to use the default toolchain, otherwise see toolchains below

# Maven Rule
MAVEN_REPOSITORY_RULES_VERSION = "1.0"
MAVEN_REPOSITORY_RULES_SHA = "5950eb0e4a3b8fd39832e58dd30e96258526751dabdc308cc7216f74396d8d41"
http_archive(
    name = "maven_repository_rules",
    urls = ["https://github.com/square/bazel_maven_repository/archive/%s.zip" % MAVEN_REPOSITORY_RULES_VERSION],
    type = "zip",
    strip_prefix = "bazel_maven_repository-%s" % MAVEN_REPOSITORY_RULES_VERSION,
    sha256 = MAVEN_REPOSITORY_RULES_SHA,
)
load("@maven_repository_rules//maven:maven.bzl", "maven_repository_specification")
maven_repository_specification(
    name = "maven",
    artifacts = {
        "androidx.annotation:annotation:1.1.0": { "sha256": "2e9372ba7780ef44952adbf86b66e1f08682c1e5277c926185f6564a13799efe" },
        "com.google.code.findbugs:jsr305:3.0.2": { "sha256": "19889dbdf1b254b2601a5ee645b8147a974644882297684c798afe5d63d78dfe"},
        "io.reactivex.rxjava2:rxjava:2.1.9": { "sha256" : "a1551d33ebbd79799d820aa13a5513877f3c08af4d2752d7fe14e0fc623cc5b8" },
        "org.reactivestreams:reactive-streams:1.0.2": {"sha256": "5b626a99e5734ba8d0c0c8c3fc6258afa0624f4ce61ae1192247d03c57463ded"}, # pinned by rxjava
        "org.jetbrains:annotations:13.0": {"sha256" : "965aeb2bedff369819bdde1bf7a0b3b89b8247dd69c88b86375d76163bb8c397"},
    },
    repository_urls = [
        "https://repo1.maven.org/maven2",
        "https://dl.google.com/dl/android/maven2/",
    ]
)

android_sdk_repository(
    name = "androidsdk",
    api_level = 28,
    build_tools_version = "28.0.3"
)