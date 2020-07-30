load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "2.4"
RULES_JVM_EXTERNAL_SHA = "2393f002b0a274055a4e803801cd078df90d1a8ac9f15748d1f803b97cfcdc9c"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
      "androidx.appcompat:appcompat:1.0.2",
    ],
    repositories = [
        "https://maven.google.com",
    ],
)

android_sdk_repository(
  name = "androidsdk",
)
