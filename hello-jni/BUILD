android_binary(
    name = "hello-jni",
    srcs = ["app/src/main/java/com/example/hellojni/HelloJni.java"],
    custom_package = "com.example.hellojni",
    manifest = "app/src/main/AndroidManifest.xml",
    # proguard_specs = ["app/proguard-rules.pro"],
    resource_files = glob(["app/src/main/res/**/*"]),
    deps = [
        ":jni",
        "@maven//:com_android_support_support_v4",
        "@maven//:com_android_support_appcompat_v7",
        "@maven//:com_android_support_constraint_constraint_layout",
    ],
)

cc_library(
    name = "jni",
    srcs = ["app/src/main/cpp/hello-jni.c"],
)
