load("//tf:tf_configure.bzl", "tf_configure")
load("//gpu:cuda_configure.bzl", "cuda_configure")

tf_configure(name = "local_config_tf")
cuda_configure(name = "local_config_cuda")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_github_grpc_grpc",
    urls = [
        "https://github.com/grpc/grpc/archive/ac1c5de1b36da4a1e3d72ca40b0e43f24266121a.tar.gz",
    ],
    strip_prefix = "grpc-ac1c5de1b36da4a1e3d72ca40b0e43f24266121a",
)

http_archive(
        name = "com_google_protobuf",
        strip_prefix = "protobuf-3.9.1",
        urls = [
            "https://github.com/protocolbuffers/protobuf/archive/v3.9.1.zip",
        ],
    )

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")
grpc_deps()
load("@com_github_grpc_grpc//bazel:grpc_extra_deps.bzl", "grpc_extra_deps")
grpc_extra_deps()
