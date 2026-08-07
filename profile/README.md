<h3 align="center">The <a href="https://wiki.debian.org/LoongArch">LoongArch</a> architecture is a RISC-style ISA developed by <a href="https://www.loongson.cn/">Loongson</a> <br> LoongArch64 is the 64-bit version of <a href="https://wiki.debian.org/LoongArch">LoongArch</a></h3>

------------------------------

## Operating Systems

| OS/Arch         | Arch      | Architecture   |
| --------------- | --------- | -------------- |
| `linux/loong64` | `loong64` | `loongarch64`  |

- **[Alpine Linux](https://www.alpinelinux.org/downloads/)**
- **[Debian GNU/Linux](https://cdimage.debian.org/cdimage/daily-builds/daily/current/loong64/iso-cd/)**

| Name                                                                                                                                                  | Description                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| [alpine-standard-3.24.1-loongarch64.iso](https://dl-cdn.alpinelinux.org/alpine/v3.24/releases/loongarch64/alpine-standard-3.24.1-loongarch64.iso)     | Alpine as it was intended. Just enough to get you started.           |
| [debian-testing-loong64-netinst.iso](https://cdimage.debian.org/cdimage/daily-builds/daily/current/loong64/iso-cd/debian-testing-loong64-netinst.iso) | Contains installer images for the non-release "ports" architectures. |

You can use **[Docker](https://docs.docker.com/get-started/get-docker/)** for quick deployment.

```bash
# Set up QEMU
docker run --privileged --rm tonistiigi/binfmt --install all
# Alpine
docker run --rm --platform linux/loong64 -it ghcr.io/loong64/alpine:3.24 sh
# Debian
docker run --rm --platform linux/loong64 -it ghcr.io/loong64/debian:trixie-slim bash
```

### Debian Packages

Install Debian packages from the **[repository](https://github.com/loong64/repo)**.

```sh
# Add the GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl

# sudo curl -fsSL "https://mirrors.loong64.com/debian-loong64-archive-keyring.gpg" -o /usr/share/keyrings/debian-loong64-archive-keyring.gpg
sudo curl -fsSL "https://loong64.github.io/repo/debian/debian-loong64-archive-keyring.gpg" -o /usr/share/keyrings/debian-loong64-archive-keyring.gpg
sudo chmod a+r /usr/share/keyrings/debian-loong64-archive-keyring.gpg

# Add the repository:
echo \
  "deb [arch=loong64 signed-by=/usr/share/keyrings/debian-loong64-archive-keyring.gpg] https://loong64.github.io/repo/debian trixie main" | \
  sudo tee /etc/apt/sources.list.d/debian-loong64-repo.list > /dev/null

# Install packages:
sudo apt update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

<details>

<summary>Package list ...</summary>

- https://loong64.github.io/repo/debian
- https://mirrors.loong64.com/debian-loong64

| Package Name              | Install Command                                     | Description                                    |
| ------------------------- | --------------------------------------------------- | ---------------------------------------------- |
| gh                        | `sudo apt install gh`                               | GitHub's official command line tool            |
| containerd.io             | `sudo apt install containerd.io`                    | An open and reliable container runtime         |
| docker-buildx-plugin      | `sudo apt install docker-buildx-plugin`             | Docker Buildx CLI plugin                       |
| docker-ce                 | `sudo apt install docker-ce`                        | Docker Engine                                  |
| docker-ce-cli             | `sudo apt install docker-ce-cli`                    | Docker CLI                                     |
| docker-ce-rootless-extras | `sudo apt install docker-ce-rootless-extras`        | Rootless support for Docker                    |
| docker-compose-plugin     | `sudo apt install docker-compose-plugin`            | Docker Compose (V2) plugin for the Docker CLI  |

</details>

More packages will be added ...

## Docker

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [Docker](https://github.com/loong64/docker-ce-packaging/releases)              | <a href="https://github.com/loong64/docker-ce-packaging"><img alt="Docker" src="https://img.shields.io/github/release/loong64/docker-ce-packaging.svg"/></a>         | Packaging scripts for Docker CE.                                                                          |
| [Containerd](https://github.com/loong64/containerd-packaging/releases)         | <a href="https://github.com/loong64/containerd-packaging"><img alt="Containerd" src="https://img.shields.io/github/release/loong64/containerd-packaging.svg"/></a>   | Linux distribution packaging for containerd.                                                              |
| [Buildx](https://github.com/loong64/buildx)                                    | <a href="https://github.com/loong64/buildx"><img alt="Buildx" src="https://img.shields.io/github/release/loong64/buildx.svg"/></a>                                   | Docker CLI plugin for extended build capabilities with BuildKit.                                          |
| [Compose](https://github.com/loong64/compose)                                  | <a href="https://github.com/loong64/compose"><img alt="Compose" src="https://img.shields.io/github/release/loong64/compose.svg"/></a>                                | Define and run multi-container applications with Docker.                                                  |
| [Plugins](https://github.com/loong64/plugins)                                  | <a href="https://github.com/loong64/plugins"><img alt="plugins" src="https://img.shields.io/github/release/loong64/plugins.svg"/></a>                                | Reference and example networking plugins maintained by the CNI team.                                      |
| [Binfmt](https://github.com/loong64/binfmt)                                    | <a href="https://github.com/loong64/binfmt"><img alt="binfmt" src="https://img.shields.io/github/release/loong64/binfmt.svg"/></a>                                   | Cross-platform emulator collection distributed with Docker images.                                        |
| [xx](https://github.com/loong64/xx)                                            | <a href="https://github.com/loong64/xx"><img alt="xx" src="https://img.shields.io/github/release/loong64/xx.svg"/></a>                                               | Dockerfile cross-compilation helpers.                                                                     |

### Docker Images

GitHub Container Registry. Images are built on **[docker-library](https://github.com/loong64/docker-library)**.

```sh
docker run --rm -it ghcr.io/loong64/golang:1.26-trixie go version
docker run --rm -it ghcr.io/loong64/node:24-trixie-slim node --version
docker run --rm -it ghcr.io/loong64/python:3.14-slim-trixie python --version
```

"Distroless" Container Images. Images are built on **[distroless](https://github.com/loong64/distroless)**.

| Image                                                                                            | Tags                                          | Architecture Suffixes                               |
| ------------------------------------------------------------------------------------------------ | --------------------------------------------- | --------------------------------------------------- |
| [ghcr.io/loong64/distroless/static-debian13](ghcr.io/loong64/distroless/static-debian13)         | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, arm, s390x, ppc64le, riscv64, loong64 |
| [ghcr.io/loong64/distroless/base-debian13](ghcr.io/loong64/distroless/base-debian13)             | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, arm, s390x, ppc64le, riscv64, loong64 |
| [ghcr.io/loong64/distroless/base-nossl-debian13](ghcr.io/loong64/distroless/base-nossl-debian13) | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, arm, s390x, ppc64le, riscv64, loong64 |
| [ghcr.io/loong64/distroless/cc-debian13](ghcr.io/loong64/distroless/cc-debian13)                 | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, arm, s390x, ppc64le, riscv64, loong64 |
| [ghcr.io/loong64/distroless/nodejs22-debian13](ghcr.io/loong64/distroless/nodejs22-debian13)     | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, arm, s390x, ppc64le, loong64          |
| [ghcr.io/loong64/distroless/nodejs24-debian13](ghcr.io/loong64/distroless/nodejs24-debian13)     | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, s390x, ppc64le, loong64               |
| [ghcr.io/loong64/distroless/nodejs26-debian13](ghcr.io/loong64/distroless/nodejs26-debian13)     | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, s390x, ppc64le, loong64               |
| [ghcr.io/loong64/distroless/python3-debian13](ghcr.io/loong64/distroless/python3-debian13)       | `latest`, `nonroot`, `debug`, `debug-nonroot` | amd64, arm64, riscv64, loong64, loong64             |

More Docker images will be added ...

## Compiler Tools

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [gcc-cross-tools](https://github.com/loong64/cross-tools)                      | <a href="https://github.com/loong64/cross-tools"><img alt="cross-tools" src="https://img.shields.io/github/release/loong64/cross-tools.svg"/></a>                    | LoongArch64 cross-compile toolchain, supports both x86_64(amd64) and aarch64(arm64) architectures.        |
| [gcc-cross-tools-musl](https://github.com/loong64/musl-cross-make)             | <a href="https://github.com/loong64/musl-cross-make"><img alt="musl-cross-make" src="https://img.shields.io/github/release/loong64/musl-cross-make.svg"/></a>        | Simple makefile-based build for musl cross compiler.                                                      |
| [clang-toolchain-tools](https://github.com/loong64/toolchain-tools)            | <a href="https://github.com/loong64/toolchain-tools"><img alt="toolchain-tools" src="https://img.shields.io/github/release/loong64/toolchain-tools.svg"/></a>        | Projects related to packaging and language toolchain support.                                             |
| [Ccache](https://github.com/loong64/ccache)                                    | <a href="https://github.com/loong64/ccache"><img alt="Ccache" src="https://img.shields.io/github/release/loong64/ccache.svg"/></a>                                   | A compiler cache.                                                                                         |
| [CMake](https://github.com/loong64/cmake)                                      | <a href="https://github.com/loong64/cmake"><img alt="CMake" src="https://img.shields.io/github/release/loong64/cmake.svg"/></a>                                      | A cross-platform, open-source build-system generator.                                                     |
| [GN](https://github.com/loong64/gn)                                            | <a href="https://github.com/loong64/gn"><img alt="gn" src="https://img.shields.io/github/release/loong64/gn.svg"/></a>                                               | A standalone version of Chromium's GN.                                                                    |
| [Ninja](https://github.com/loong64/ninja)                                      | <a href="https://github.com/loong64/ninja"><img alt="Ninja" src="https://img.shields.io/github/release/loong64/ninja.svg"/></a>                                      | A small build system focused on speed.                                                                    |

### Dart

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [dart](https://github.com/dart-loong64/dart)                                   | <a href="https://github.com/dart-loong64/dart"><img alt="Vite+" src="https://img.shields.io/github/release/dart-loong64/dart.svg"/></a>                              | The Dart SDK.                                                                                             |
| [dart-musl](https://github.com/dart-loong64/dart-musl)                         | <a href="https://github.com/dart-loong64/dart-musl"><img alt="Vite+" src="https://img.shields.io/github/release/dart-loong64/dart-musl.svg"/></a>                    | The Dart SDK (musl).                                                                                      |
| [dart-sass](https://github.com/loong64/dart-sass)                              | <a href="https://github.com/loong64/dart-sass"><img alt="dart-sass" src="https://img.shields.io/github/release/loong64/dart-sass.svg"/></a>                          | The reference implementation of Sass, written in Dart.                                                    |


## Python

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [uv](https://github.com/loong64/uv)                                            | <a href="https://github.com/loong64/uv"><img alt="uv" src="https://img.shields.io/github/release/loong64/uv.svg"/></a>                                               | An extremely fast Python package and project manager written in Rust.                                     |
| [python-build-standalone](https://github.com/loong64/python-build-standalone) | <a href="https://github.com/loong64/python-build-standalone"><img alt="Python" src="https://img.shields.io/github/release/loong64/python-build-standalone.svg"/></a> | Produce redistributable Python builds.                                                                    |

```sh
wget -O - https://github.com/loong64/uv/releases/latest/download/uv-loongarch64-unknown-linux-gnu.tar.gz | tar xz --strip-components=1 -C /usr/local/bin
uv --version

cd ~/project

export UV_EXTRA_INDEX_URL=https://mirrors.loong64.com/pypi/simple
# uv venv --python <version> <path>
uv venv --python 3.11 .venv
uv run python --version

# uv pip install "SomePackage"
uv pip install django
```

#### PyPI Repository

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [PyTorch](https://github.com/loong64/pytorch)                                  | <a href="https://github.com/loong64/pytorch"><img alt="PyTorch" src="https://img.shields.io/github/release/loong64/pytorch.svg"/></a>                                | Tensors and Dynamic neural networks in Python with strong GPU acceleration.                               |
| [TensorFlow](https://github.com/loong64/tensorflow)                            | <a href="https://github.com/loong64/pytorch"><img alt="TensorFlow" src="https://img.shields.io/github/release/loong64/tensorflow.svg"/></a>                          | An Open Source Machine Learning Framework for Everyone.                                                   |
| [ONNX Runtime](https://github.com/loong64/maturin)                             | <a href="https://github.com/loong64/onnxruntime"><img alt="ONNX Runtime" src="https://img.shields.io/github/release/loong64/onnxruntime.svg"/></a>                   | ONNX Runtime: cross-platform, high performance ML inferencing and training accelerator.                   |

Python Package Index. **[PyPI](https://github.com/loong64/pypi)**

```sh
export PIP_EXTRA_INDEX_URL=https://mirrors.loong64.com/pypi/simple
pip install -U pip

# pip install "SomePackage"
pip install uv
```

More packages will be added ...

### Node.js

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [Node.js](https://github.com/loong64/node/releases)                            | <a href="https://github.com/loong64/node/releases"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/node.svg"/></a>                             | Node.js JavaScript runtime.                                                                               |
| [isolated-vm](https://github.com/loong64/isolated-vm)                          | <a href="https://github.com/loong64/isolated-vm"><img alt="isolated-vm" src="https://img.shields.io/github/release/loong64/isolated-vm.svg"/></a>                    | Secure & isolated JS environments for nodejs.                                                             |
| [node-sqlite3](https://github.com/loong64/node-sqlite3)                        | <a href="https://github.com/loong64/node-sqlite3"><img alt="node-sqlite3" src="https://img.shields.io/github/release/loong64/node-sqlite3.svg"/></a>                 | SQLite3 bindings for Node.js.                                                                             |
| [Tailwind CSS](https://github.com/loong64/tailwindcss)                         | <a href="https://github.com/loong64/tailwindcss"><img alt="Tailwind CSS" src="https://img.shields.io/github/release/loong64/tailwindcss.svg"/></a>                   | A utility-first CSS framework for rapid UI development..                                                  |
| [Lightning CSS](https://github.com/loong64/lightningcss)                       | <a href="https://github.com/loong64/lightningcss"><img alt="Lightning CSS" src="https://img.shields.io/github/release/loong64/lightningcss.svg"/></a>                | An extremely fast CSS parser, transformer, bundler, and minifier written in Rust..                        |
| [Tauri](https://github.com/loong64/tauri)                                      | <a href="https://github.com/loong64/tauri"><img alt="Tauri" src="https://img.shields.io/github/release/loong64/tauri.svg"/></a>                                      | Build smaller, faster, and more secure desktop and mobile applications with a web frontend.               |
| [Next.js](https://github.com/loong64/next.js)                                  | <a href="https://github.com/loong64/next.js"><img alt="Next.js" src="https://img.shields.io/github/release/loong64/next.js.svg"/></a>                                | The React Framework.                                                                                      |
| [Vite+](https://github.com/loong64/vite-plus)                                  | <a href="https://github.com/loong64/vite-plus"><img alt="Vite+" src="https://img.shields.io/github/release/loong64/vite-plus.svg"/></a>                              | Vite+ is the unified toolchain and entry point for web development.                                       |

### Applications

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [gosu](https://github.com/loong64/gosu)                                        | <a href="https://github.com/loong64/gosu"><img alt="gosu" src="https://img.shields.io/github/release/loong64/gosu.svg"/></a>                                         | Simple Go-based setuid, setgid, setgroups, and exec tool.                                                 |
| [ossutil](https://github.com/loong64/ossutil)                                  | <a href="https://github.com/loong64/ossutil"><img alt="ossutil" src="https://img.shields.io/github/release/loong64/ossutil.svg"/></a>                                | A user-friendly command-line tool for accessing Alibaba Cloud OSS.                                        |
| [llama.cpp](https://github.com/loong64/llama.cpp)                              | <a href="https://github.com/loong64/llama.cpp"><img alt="llama.cpp" src="https://img.shields.io/github/release/loong64/llama.cpp.svg"/></a>                          | LLM inference in C/C++.                                                                                   |
| [Ollama](https://github.com/loong64/ollama)                                    | <a href="https://github.com/loong64/ollama"><img alt="Ollama" src="https://img.shields.io/github/release/loong64/ollama.svg"/></a>                                   | Get up and running with large language models.                                                            |
| [Godot](https://github.com/loong64/godot)                                      | <a href="https://github.com/loong64/godot"><img alt="Godot" src="https://img.shields.io/github/release/loong64/godot.svg"/></a>                                      | A multi-platform 2D and 3D game engine.                                                                   |
| [Box64](https://github.com/loong64/box64)                                      | <a href="https://github.com/loong64/box64"><img alt="Box64" src="https://img.shields.io/github/release/loong64/box64.svg"/></a>                                      | A Linux userspace x86_64 emulator.                                                                        |
| [Cosign](https://github.com/loong64/cosign)                                    | <a href="https://github.com/loong64/cosign"><img alt="Cosign" src="https://img.shields.io/github/release/loong64/cosign.svg"/></a>                                   | Code signing and transparency for containers and binaries.                                                |
| [GitHub CLI](https://github.com/loong64/cli)                                   | <a href="https://github.com/loong64/cli"><img alt="CLI" src="https://img.shields.io/github/release/loong64/cli.svg"/></a>                                            | GitHub's official command-line tool.                                                                      |
| [GitHub Actions Runner](https://github.com/loong64/runner)                     | <a href="https://github.com/loong64/runner"><img alt="CLI" src="https://img.shields.io/github/v/release/loong64/runner.svg"/></a>                                    | The runner for GitHub Actions.                                                                            |
| [AppImageTool](https://github.com/loong64/appimagetool)                        | <a href="https://github.com/loong64/appimagetool"><img alt="appimagetool" src="https://img.shields.io/github/release/loong64/appimagetool.svg"/></a>                 | A low-level tool for generating an AppImage from an existing AppDir.                                      |
| [Nydus](https://github.com/loong64/nydus)                                      | <a href="https://github.com/loong64/nydus"><img alt="Nydus" src="https://img.shields.io/github/release/loong64/nydus.svg"/></a>                                      | Dragonfly image service.                                                                                  |
| [DuckDB](https://github.com/loong64/duckdb)                                    | <a href="https://github.com/loong64/duckdb"><img alt="DuckDB" src="https://img.shields.io/github/release/loong64/duckdb.svg"/></a>                                   | DuckDB is an analytical in-process SQL database management system.                                        |

## Links

<a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=XZj-dzRYq2BTQ_SulR3VHZ0dLO1XI7ek&jump_from=webapi&authKey=+DqUmM7wBsAOTWNI6+zu0ZCyIgav4WUu4evgRJAqvakDOr9iB4paFolaE0fWDiq2"><img border="0" src="https://pub.idqqimg.com/wpa/images/group.png" alt="LoongArch64 开源交流群" title="LoongArch64 开源交流群"></a>
