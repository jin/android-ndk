android_binary(
    name = "nn_sample",
    srcs = ["app/src/main/java/com/example/android/nnapidemo/MainActivity.java"],
    custom_package = "com.example.android.nnapidemo",
    manifest = "app/src/main/AndroidManifest.xml",
    # proguard_specs = ["app/proguard-rules.pro"],
    resource_files = glob(["app/src/main/res/**/*"]),
    assets = glob(["app/src/main/assets/**"]),
    assets_dir = "app/src/main/assets",
    deps = [
        "model",
        "@maven//:com_android_support_support_v4",
        "@maven//:com_android_support_appcompat_v7",
        "@maven//:com_android_support_constraint_constraint_layout",
    ],
)

cc_library(
    name = "model",
    srcs = [
        "app/src/main/cpp/nn_sample.cpp",
        "app/src/main/cpp/simple_model.cpp",
    ],
    hdrs = [
        "app/src/main/cpp/simple_model.h",
    ],
    linkopts = [
        "-landroid",
        "-llog",
        "-lneuralnetworks",
    ]
)
