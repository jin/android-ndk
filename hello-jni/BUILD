load("@gmaven_rules//:defs.bzl", "gmaven_artifact")

android_binary(
    name = "hello-jni",
    srcs = ["app/src/main/java/com/example/hellojni/HelloJni.java"],
    custom_package = "com.example.hellojni",
    manifest = "app/src/main/AndroidManifest.xml",
    proguard_specs = ["app/proguard-rules.pro"],
    resource_files = glob(["app/src/main/res/**/*"]),
    deps = [
        ":jni",
        gmaven_artifact("com.android.support:appcompat-v7:aar:25.4.0"),
        gmaven_artifact("com.android.support.constraint:constraint-layout:aar:1.0.2"),
    ],
)

cc_library(
    name = "jni",
    srcs = ["app/src/main/cpp/hello-jni.c"],
)
