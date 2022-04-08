workspace(name = "bazel-containers")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "85ffff62a4c22a74dbd98d05da6cf40f497344b3dbf1e1ab0a37ab2a1a6ca014",
    strip_prefix = "rules_docker-0.23.0",
    urls = ["https://github.com/bazelbuild/rules_docker/releases/download/v0.23.0/rules_docker-v0.23.0.tar.gz"],
)

load(
    "@io_bazel_rules_docker//repositories:repositories.bzl",
    container_repositories = "repositories",
)
container_repositories()


load("@io_bazel_rules_docker//repositories:deps.bzl", container_deps = "deps")
container_deps()

load(
    "@io_bazel_rules_docker//python:image.bzl",
    _py_image_repos = "repositories",
)

_py_image_repos()

# 
# load(
#     "@io_bazel_rules_docker//repositories:go_repositories.bzl",
#     container_go_deps = "go_deps",
# )
# 
# container_go_deps()
# 
# load("@io_bazel_rules_docker//container:pull.bzl", "container_pull")
# load("@io_bazel_rules_docker//contrib:dockerfile_build.bzl", "dockerfile_image")
# load("@io_bazel_rules_docker//java:image.bzl", _java_image_repos = "repositories")
# 
# _java_image_repos()
# 
# container_pull(
#     name = "alpine_linux_amd64",
#     digest = "sha256:954b378c375d852eb3c63ab88978f640b4348b01c1b3456a024a81536dafbbf4",
#     registry = "index.docker.io",
#     repository = "library/alpine",
#     # tag field is ignored since digest is set
#     tag = "3.8",
# )
# 
# container_pull(
#     name = "ubuntu1604",
#     digest = "sha256:8f0b64fd212007183434b8b3271b723700ab14e4230b5bec1415b79aaa3ac97b",
#     registry = "l.gcr.io",
#     repository = "google/ubuntu1604",
#     # tag field is ignored since digest is set
#     tag = "latest",
# )
# 
# container_pull(
#     name = "bazel_image",
#     digest = "sha256:ace9881e6e9c5d48b5fd637321361aeffe54000265894a65f7d818dc1065bd80",
#     registry = "launcher.gcr.io",
#     repository = "google/bazel",
# )
# 
# dockerfile_image(
#     name = "basic_alpine_dockerfile",
#     dockerfile = "//basic:Dockerfile",
# )
# 
# dockerfile_image(
#     name = "extended_alpine_dockerfile",
#     dockerfile = "//extended:Dockerfile",
# )
# 
# dockerfile_image(
#     name = "java_python_dockerfile",
#     dockerfile = "//run_instruction_apt_pkgs:Dockerfile",
# )
# 
# dockerfile_image(
#     name = "bazel_gcloud_dockerfile",
#     dockerfile = "//run_instruction_arbitrary:Dockerfile",
# )
# 
# dockerfile_image(
#     name = "java_app_dockerfile",
#     dockerfile = "//java_app:Dockerfile",
# )
# 
# http_file(
#     name = "gcloud_archive",
#     downloaded_file_path = "google-cloud-sdk.tar.gz",
#     sha256 = "a2205e35b11136004d52d47774762fbec9145bf0bda74ca506f52b71452c570e",
#     urls = [
#         "https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-220.0.0-linux-x86_64.tar.gz",
#     ],
# )
