package(default_visibility = ["//visibility:public"])

licenses(["by_exception_only"])

exports_files(["LICENSE"])

cc_library(
    name = "vrapi",
    srcs = select({
        "@tools//target_cpu:arm64-v8a": [
            "Libs/Android/arm64-v8a/Release/libvrapi.so",
        ],
        "@tools//target_cpu:armeabi-v7a": [
            "Libs/Android/armeabi-v7a/Release/libvrapi.so",
        ],
        "//conditions:default": [],
    }),
    hdrs = glob([
        "Include/*.h",
    ]),
)

cc_library(
    name = "vrapi_debug",
    srcs = select({
        "@tools//target_cpu:arm64-v8a": [
            "Libs/Android/arm64-v8a/Debug/libvrapi.so",
        ],
        "@tools//target_cpu:armeabi-v7a": [
            "Libs/Android/armeabi-v7a/Debug/libvrapi.so",
        ],
        "//conditions:default": [],
    }),
    hdrs = glob([
        "Include/*.h",
    ]),
    visibility = ["//third_party/oculus/mobile:__subpackages__"],
)
