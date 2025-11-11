<h3 align="center">The <a href="https://wiki.debian.org/LoongArch">LoongArch</a> architecture is a RISC-style ISA developed by <a href="https://www.loongson.cn/">Loongson</a> <br> LoongArch64 is the 64-bit version of <a href="https://wiki.debian.org/LoongArch">LoongArch</a></h3>

------------------------------

## Quick Start

| OS/Arch         | Arch      | Architecture   |
| --------------- | --------- | -------------- |
| `linux/loong64` | `loong64` | `loongarch64`  |

You can use **[Docker](https://docs.docker.com/get-started/get-docker/)** to quickly deploy.

```bash
# Set up QEMU
docker run --privileged --rm tonistiigi/binfmt --install all

# Alpine
docker run --rm --platform linux/loong64 -it ghcr.io/loong64/alpine:3.22 sh

# Debian
docker run --rm --platform linux/loong64 -it ghcr.io/loong64/debian:trixie-slim bash
```

Or use Linux OS to boot.

- **[Alpine Linux](https://www.alpinelinux.org/downloads/)** 
- **[Debian GNU/Linux](https://cdimage.debian.org/cdimage/ports/snapshots/2025-08-29/)** 

| Name                                                                                                                                              | Description                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| [alpine-standard-3.22.2-loongarch64.iso](https://dl-cdn.alpinelinux.org/alpine/v3.22/releases/loongarch64/alpine-standard-3.22.2-loongarch64.iso) | Alpine as it was intended. Just enough to get you started.           |
| [debian-12.0.0-loong64-NETINST-1.iso](https://cdimage.debian.org/cdimage/ports/snapshots/2025-08-29/debian-12.0.0-loong64-NETINST-1.iso)          | contains installer images for the non-release "ports" architectures. |

## Applications

Binary applications.

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [gn](https://github.com/loong64/gn)                                            | <a href="https://github.com/loong64/gn"><img alt="gn" src="https://img.shields.io/github/release/loong64/gn.svg"/></a>                                               | Standalone version of Chromium's GN.                                                                      |
| [uv](https://github.com/loong64/uv)                                            | <a href="https://github.com/loong64/uv"><img alt="uv" src="https://img.shields.io/github/release/loong64/uv.svg"/></a>                                               | An extremely fast Python package and project manager, written in Rust.                                    |
| [gosu](https://github.com/loong64/gosu)                                        | <a href="https://github.com/loong64/gosu"><img alt="gosu" src="https://img.shields.io/github/release/loong64/gosu.svg"/></a>                                         | Simple Go-based setuid+setgid+setgroups+exec.                                                             |
| [ninja](https://github.com/loong64/ninja)                                      | <a href="https://github.com/loong64/ninja"><img alt="ninja" src="https://img.shields.io/github/release/loong64/ninja.svg"/></a>                                      | a small build system with a focus on speed.                                                               |
| [binfmt](https://github.com/loong64/binfmt)                                    | <a href="https://github.com/loong64/binfmt"><img alt="binfmt" src="https://img.shields.io/github/release/loong64/binfmt.svg"/></a>                                   | Cross-platform emulator collection distributed with Docker images.                                        |
| [buildx](https://github.com/loong64/buildx)                                    | <a href="https://github.com/loong64/buildx"><img alt="buildx" src="https://img.shields.io/github/release/loong64/buildx.svg"/></a>                                   | Docker CLI plugin for extended build capabilities with BuildKit.                                          |
| [compose](https://github.com/loong64/compose)                                  | <a href="https://github.com/loong64/compose"><img alt="compose" src="https://img.shields.io/github/release/loong64/compose.svg"/></a>                                | Define and run multi-container applications with Docker.                                                  |
| [ossutil](https://github.com/loong64/ossutil)                                  | <a href="https://github.com/loong64/ossutil"><img alt="ossutil" src="https://img.shields.io/github/release/loong64/ossutil.svg"/></a>                                | A user friendly command line tool to access AliCloud OSS.                                                 |
| [plugins](https://github.com/loong64/plugins)                                  | <a href="https://github.com/loong64/plugins"><img alt="plugins" src="https://img.shields.io/github/release/loong64/plugins.svg"/></a>                                | Some reference and example networking plugins, maintained by the CNI team.                                |
| [llama.cpp](https://github.com/loong64/llama.cpp)                              | <a href="https://github.com/loong64/llama.cpp"><img alt="llama.cpp" src="https://img.shields.io/github/release/loong64/llama.cpp.svg"/></a>                          | LLM inference in C/C++.                                                                                   |
| [cross-tools](https://github.com/loong64/cross-tools)                          | <a href="https://github.com/loong64/cross-tools"><img alt="cross-tools" src="https://img.shields.io/github/release/loong64/cross-tools.svg"/></a>                    | LoongArch64 cross-compile toolchain, supports both x86_64(amd64) and aarch64(arm64) architectures.        |
| [cibuildwheel](https://github.com/loong64/cibuildwheel)                        | <a href="https://github.com/loong64/cibuildwheel"><img alt="cibuildwheel" src="https://img.shields.io/github/release/loong64/cibuildwheel.svg"/></a>                 | 🎡 Build Python wheels for all the platforms with minimal configuration.                                 |
| [node-sqlite3](https://github.com/loong64/node-sqlite3)                        | <a href="https://github.com/loong64/node-sqlite3"><img alt="node-sqlite3" src="https://img.shields.io/github/release/loong64/node-sqlite3.svg"/></a>                 | SQLite3 bindings for Node.js.                                                                             |
| [Box64](https://github.com/loong64/box64)                                      | <a href="https://github.com/loong64/box64"><img alt="Box64" src="https://img.shields.io/github/release/loong64/box64.svg"/></a>                                      | Linux Userspace x86_64 Emulator with a twist.                                                             |
| [Cosign](https://github.com/loong64/cosign)                                    | <a href="https://github.com/loong64/cosign"><img alt="Cosign" src="https://img.shields.io/github/release/loong64/cosign.svg"/></a>                                   | Code signing and transparency for containers and binaries.                                                |
| [CMake](https://github.com/loong64/cmake)                                      | <a href="https://github.com/loong64/cmake"><img alt="CMake" src="https://img.shields.io/github/release/loong64/cosign.svg"/></a>                                     | CMake is a cross-platform, open-source build system generator.                                            |
| [Docker](https://github.com/loong64/docker-ce-packaging/releases)              | <a href="https://github.com/loong64/docker-ce-packaging"><img alt="Docker" src="https://img.shields.io/github/release/loong64/docker-ce-packaging.svg"/></a>         | Packaging scripts for Docker CE                                                                           |
| [Ollama](https://github.com/loong64/ollama)                                    | <a href="https://github.com/loong64/ollama"><img alt="Ollama" src="https://img.shields.io/github/release/loong64/ollama.svg"/></a>                                   | Get up and running with large language models.                                                            |
| [Maturin](https://github.com/loong64/maturin)                                  | <a href="https://github.com/loong64/maturin"><img alt="Maturin" src="https://img.shields.io/github/release/loong64/maturin.svg"/></a>                                | Build and publish crates with pyo3, cffi and uniffi bindings as well as rust binaries as python packages. |
| [Nydus](https://github.com/loong64/nydus)                                      | <a href="https://github.com/loong64/nydus"><img alt="Nydus" src="https://img.shields.io/github/release/loong64/nydus.svg"/></a>                                      | the Dragonfly image service.                                                                              |
| [PyTorch](https://github.com/loong64/pytorch)                                  | <a href="https://github.com/loong64/pytorch"><img alt="PyTorch" src="https://img.shields.io/github/release/loong64/pytorch.svg"/></a>                                | Tensors and Dynamic neural networks in Python with strong GPU acceleration.                               |
| [Node.js](https://github.com/loong64/node/releases)                            | <a href="https://github.com/loong64/node/releases"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/node.svg"/></a>                             | Node.js JavaScript runtime ✨🐢🚀✨                                                                     |
| [GitHub CLI](https://github.com/loong64/cli)                                   | <a href="https://github.com/loong64/cli"><img alt="CLI" src="https://img.shields.io/github/release/loong64/cli.svg"/></a>                                            | GitHub’s official command line tool                                                                       |
| [GitHub Actions  Runner](https://github.com/loong64/cli)                       | <a href="https://github.com/loong64/runner"><img alt="CLI" src="https://img.shields.io/github/v/release/loong64/runner.svg"/></a>                                    | The Runner for GitHub Actions 🚀                                                                      |
| [Containerd](https://github.com/loong64/containerd-packaging/releases)         | <a href="https://github.com/loong64/containerd-packaging"><img alt="Containerd" src="https://img.shields.io/github/release/loong64/containerd-packaging.svg"/></a>   | Linux distro packaging for containerd                                                                     |
| [Python Standalone Builds](https://github.com/loong64/python-build-standalone) | <a href="https://github.com/loong64/python-build-standalone"><img alt="Python" src="https://img.shields.io/github/release/loong64/python-build-standalone.svg"/></a> | Produce redistributable builds of Python                                                                  |

## Docker Images

GitHub Container Registry. Images are built on **[docker-library](https://github.com/loong64/docker-library)**

```sh
docker run --rm -it ghcr.io/loong64/golang:1.24-trixie go version
docker run --rm -it ghcr.io/loong64/node:24-trixie-slim node --version
docker run --rm -it ghcr.io/loong64/python:3.13-slim-trixie python --version
```

More Docker images will be added ...

## Debian Packages

Install Debian Packages **[repo](https://github.com/loong64/repo)**

```sh
# Add GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl

sudo curl -fsSL "https://mirrors.loong64.com/debian/debian-loong64-archive-keyring.gpg" -o /usr/share/keyrings/debian-loong64-archive-keyring.gpg
sudo chmod a+r /usr/share/keyrings/debian-loong64-archive-keyring.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch=loong64 signed-by=/usr/share/keyrings/debian-loong64-archive-keyring.gpg] https://mirrors.loong64.com/debian trixie main" | \
  sudo tee /etc/apt/sources.list.d/debian-loong64-repo.list > /dev/null

# Install the Docker packages.
sudo apt update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

<details>

<summary>Details ...</summary>

----
Package List

- https://mirrors.loong64.com/debian
- https://loong64.github.io/repo/debian

| Package Name              | Install Command                                     | Description                                    |
| ------------------------- | --------------------------------------------------- | ---------------------------------------------- |
| gh                        | `sudo apt install gh`                               | GitHub's official command line tool            |
| latx                      | `sudo apt install latx-i386 latx-amd64 latx-common` | Loongson Architecture Translator for x86       |
| box64                     | `sudo apt install box64`                            | Linux Userspace x86_64 Emulator with a twist.  |
| containerd.io             | `sudo apt install containerd.io`                    | An open and reliable container runtime         |
| docker-buildx-plugin      | `sudo apt install docker-buildx-plugin`             | Docker Buildx CLI plugin                       |
| docker-ce                 | `sudo apt install docker-ce`                        | Docker Engine                                  |
| docker-ce-cli             | `sudo apt install docker-ce-cli`                    | Docker CLI                                     |
| docker-ce-rootless-extras | `sudo apt install docker-ce-rootless-extras`        | Rootless support for Docker                    |
| docker-compose-plugin     | `sudo apt install docker-compose-plugin`            | Docker Compose (V2) plugin for the Docker CLI  |

</details>

More packages will be added ...

## PyPI Repository

Python Package Index. **[pypi](https://github.com/loong64/pypi)**

```sh
# pip install "SomeProject" --extra-index-url https://mirrors.loong64.com/pypi/simple
pip install uv --extra-index-url https://mirrors.loong64.com/pypi/simple
```

More packages will be added ...

## Links

<a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=XZj-dzRYq2BTQ_SulR3VHZ0dLO1XI7ek&jump_from=webapi&authKey=+DqUmM7wBsAOTWNI6+zu0ZCyIgav4WUu4evgRJAqvakDOr9iB4paFolaE0fWDiq2"><img border="0" src="https://pub.idqqimg.com/wpa/images/group.png" alt="LoongArch64 开源交流群" title="LoongArch64 开源交流群"></a>
