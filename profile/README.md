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
- **[Debian GNU/Linux](https://cdimage.debian.org/cdimage/ports/snapshots/2025-04-01/)** 

| Name                                                                                                                                              | Description                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| [alpine-standard-3.22.0-loongarch64.iso](https://dl-cdn.alpinelinux.org/alpine/v3.22/releases/loongarch64/alpine-standard-3.22.0-loongarch64.iso) | Alpine as it was intended. Just enough to get you started.           |
| [debian-12.0.0-loong64-NETINST-1.iso](https://cdimage.debian.org/cdimage/ports/snapshots/2025-04-01/debian-12.0.0-loong64-NETINST-1.iso)          | contains installer images for the non-release "ports" architectures. |

## Applications

Binary applications.

| Name                                                                           | Release                                                                                                                                                              | Description                                                                                               |
| ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [uv](https://github.com/loong64/uv)                                            | <a href="https://github.com/loong64/uv"><img alt="uv" src="https://img.shields.io/github/release/loong64/uv.svg"/></a>                                               | An extremely fast Python package and project manager, written in Rust.                                    |
| [xx](https://github.com/loong64/xx)                                            | <a href="https://github.com/loong64/xx"><img alt="xx" src="https://img.shields.io/github/release/loong64/xx.svg"/></a>                                               | Dockerfile cross-compilation helpers.                                                                     |
| [gosu](https://github.com/loong64/gosu)                                        | <a href="https://github.com/loong64/gosu"><img alt="gosu" src="https://img.shields.io/github/release/loong64/gosu.svg"/></a>                                         | Simple Go-based setuid+setgid+setgroups+exec.                                                             |
| [ninja](https://github.com/loong64/ninja)                                      | <a href="https://github.com/loong64/ninja"><img alt="ninja" src="https://img.shields.io/github/release/loong64/ninja.svg"/></a>                                      | a small build system with a focus on speed.                                                               |
| [binfmt](https://github.com/loong64/binfmt)                                    | <a href="https://github.com/loong64/binfmt"><img alt="binfmt" src="https://img.shields.io/github/release/loong64/binfmt.svg"/></a>                                   | Cross-platform emulator collection distributed with Docker images.                                        |
| [buildx](https://github.com/loong64/buildx)                                    | <a href="https://github.com/loong64/buildx"><img alt="buildx" src="https://img.shields.io/github/release/loong64/buildx.svg"/></a>                                   | Docker CLI plugin for extended build capabilities with BuildKit.                                          |
| [compose](https://github.com/loong64/compose)                                  | <a href="https://github.com/loong64/compose"><img alt="compose" src="https://img.shields.io/github/release/loong64/compose.svg"/></a>                                | Define and run multi-container applications with Docker.                                                  |
| [ossutil](https://github.com/loong64/ossutil)                                  | <a href="https://github.com/loong64/ossutil"><img alt="ossutil" src="https://img.shields.io/github/release/loong64/ossutil.svg"/></a>                                | A user friendly command line tool to access AliCloud OSS.                                                 |
| [plugins](https://github.com/loong64/plugins)                                  | <a href="https://github.com/loong64/plugins"><img alt="plugins" src="https://img.shields.io/github/release/loong64/plugins.svg"/></a>                                | Some reference and example networking plugins, maintained by the CNI team.                                |
| [cloudreve](https://github.com/loong64/cloudreve)                              | <a href="https://github.com/loong64/cloudreve"><img alt="cloudreve" src="https://img.shields.io/github/release/loong64/cloudreve.svg"/></a>                          | 🌩 Self-hosted file management and sharing system, supports multiple storage providers.                   |
| [llama.cpp](https://github.com/loong64/llama.cpp)                              | <a href="https://github.com/loong64/llama.cpp"><img alt="llama.cpp" src="https://img.shields.io/github/release/loong64/llama.cpp.svg"/></a>                          | LLM inference in C/C++.                                                                                   |
| [cross-tools](https://github.com/loong64/cross-tools)                          | <a href="https://github.com/loong64/cross-tools"><img alt="cross-tools" src="https://img.shields.io/github/release/loong64/cross-tools.svg"/></a>                    | LoongArch64 cross-compile toolchain, supports both x86_64(amd64) and aarch64(arm64) architectures.        |
| [cibuildwheel](https://github.com/loong64/cibuildwheel)                        | <a href="https://github.com/loong64/cibuildwheel"><img alt="cibuildwheel" src="https://img.shields.io/github/release/loong64/cibuildwheel.svg"/></a>                 | 🎡 Build Python wheels for all the platforms with minimal configuration.                                 |
| [node-sqlite3](https://github.com/loong64/node-sqlite3)                        | <a href="https://github.com/loong64/node-sqlite3"><img alt="node-sqlite3" src="https://img.shields.io/github/release/loong64/node-sqlite3.svg"/></a>                 | SQLite3 bindings for Node.js.                                                                             |
| [Box64](https://github.com/loong64/box64)                                      | <a href="https://github.com/loong64/box64"><img alt="Box64" src="https://img.shields.io/github/release/loong64/box64.svg"/></a>                                      | Linux Userspace x86_64 Emulator with a twist.                                                             |
| [Cosign](https://github.com/loong64/cosign)                                    | <a href="https://github.com/loong64/cosign"><img alt="Cosign" src="https://img.shields.io/github/release/loong64/cosign.svg"/></a>                                   | Code signing and transparency for containers and binaries.                                                |
| [Docker](https://github.com/loong64/docker-ce-packaging/releases)              | <a href="https://github.com/loong64/docker-ce-packaging"><img alt="Docker" src="https://img.shields.io/github/release/loong64/docker-ce-packaging.svg"/></a>         | Packaging scripts for Docker CE                                                                           |
| [Ollama](https://github.com/loong64/ollama)                                    | <a href="https://github.com/loong64/ollama"><img alt="Ollama" src="https://img.shields.io/github/release/loong64/ollama.svg"/></a>                                   | Get up and running with large language models.                                                            |
| [Maturin](https://github.com/loong64/maturin)                                  | <a href="https://github.com/loong64/maturin"><img alt="Maturin" src="https://img.shields.io/github/release/loong64/maturin.svg"/></a>                                | Build and publish crates with pyo3, cffi and uniffi bindings as well as rust binaries as python packages. |
| [PyTorch](https://github.com/loong64/pytorch)                                  | <a href="https://github.com/loong64/pytorch"><img alt="PyTorch" src="https://img.shields.io/github/release/loong64/pytorch.svg"/></a>                                | Tensors and Dynamic neural networks in Python with strong GPU acceleration.                               |
| [Node.js](https://github.com/loong64/node/releases)                            | <a href="https://github.com/loong64/node/releases"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/node.svg"/></a>                             | Node.js JavaScript runtime ✨🐢🚀✨                                                                     |
| [OpenList](https://github.com/loong64/OpenList)                                | <a href="https://github.com/loong64/OpenList/releases"><img alt="OpenList" src="https://img.shields.io/github/release/loong64/OpenList.svg"/></a>                    | A new AList Fork to Anti Trust Crisis                                                                     |
| [Cloudreve](https://github.com/loong64/Cloudreve/releases)                     | <a href="https://github.com/loong64/Cloudreve/releases"><img alt="Cloudreve" src="https://img.shields.io/github/release/loong64/Cloudreve.svg"/></a>                 | 🌩 Self-hosted file management and sharing system, supports multiple storage providers                    |
| [GitHub CLI](https://github.com/loong64/cli)                                   | <a href="https://github.com/loong64/cli"><img alt="CLI" src="https://img.shields.io/github/release/loong64/cli.svg"/></a>                                            | GitHub’s official command line tool                                                                       |
| [Containerd](https://github.com/loong64/containerd-packaging/releases)         | <a href="https://github.com/loong64/containerd-packaging"><img alt="Containerd" src="https://img.shields.io/github/release/loong64/containerd-packaging.svg"/></a>   | Linux distro packaging for containerd                                                                     |
| [Python Standalone Builds](https://github.com/loong64/python-build-standalone) | <a href="https://github.com/loong64/python-build-standalone"><img alt="Python" src="https://img.shields.io/github/release/loong64/python-build-standalone.svg"/></a> | Produce redistributable builds of Python                                                                  |

## Docker Images

GitHub Container Registry. Images are built on **[docker-library](https://github.com/loong64/docker-library)**

```sh
docker run --rm -it ghcr.io/loong64/golang:1.24-trixie go version
docker run --rm -it ghcr.io/loong64/node:23-trixie-slim node --version
docker run --rm -it ghcr.io/loong64/python:3.13-slim-trixie python --version
```

<details>

<summary>Details ...</summary>

----

| Name                                                     | Tag                  | Pull Command                                             |
| -------------------------------------------------------- | -------------------- | -------------------------------------------------------- |
| [alpine](https://ghcr.io/loong64/alpine)                 | `3.21`               | `docker pull ghcr.io/loong64/alpine:3.21`                |
| [alpine](https://ghcr.io/loong64/alpine)                 | `3.22`               | `docker pull ghcr.io/loong64/alpine:3.22`                |
| [debian](https://ghcr.io/loong64/debian)                 | `trixie`             | `docker pull ghcr.io/loong64/debian:trixie`              |
| [debian](https://ghcr.io/loong64/debian)                 | `trixie-slim`        | `docker pull ghcr.io/loong64/debian:trixie-slim`         |
| [buildpack-deps](https://ghcr.io/loong64/buildpack-deps) | `trixie`             | `docker pull ghcr.io/loong64/buildpack-deps:trixie`      |
| [buildpack-deps](https://ghcr.io/loong64/buildpack-deps) | `trixie-scm`         | `docker pull ghcr.io/loong64/buildpack-deps:trixie-scm`  |
| [buildpack-deps](https://ghcr.io/loong64/buildpack-deps) | `trixie-curl`        | `docker pull ghcr.io/loong64/buildpack-deps:trixie-curl` |
| [golang](https://ghcr.io/loong64/golang)                 | `1.23-alpine`        | `docker pull ghcr.io/loong64/golang:1.23-alpine`         |
| [golang](https://ghcr.io/loong64/golang)                 | `1.23-trixie`        | `docker pull ghcr.io/loong64/golang:1.23-trixie`         |
| [golang](https://ghcr.io/loong64/golang)                 | `1.24-alpine`        | `docker pull ghcr.io/loong64/golang:1.24-alpine`         |
| [golang](https://ghcr.io/loong64/golang)                 | `1.24-trixie`        | `docker pull ghcr.io/loong64/golang:1.24-trixie`         |
| [node](https://ghcr.io/loong64/node)                     | `18-alpine`          | `docker pull ghcr.io/loong64/node:18-alpine`             |
| [node](https://ghcr.io/loong64/node)                     | `18-trixie`          | `docker pull ghcr.io/loong64/node:18-trixie`             |
| [node](https://ghcr.io/loong64/node)                     | `18-trixie-slim`     | `docker pull ghcr.io/loong64/node:18-trixie-slim`        |
| [node](https://ghcr.io/loong64/node)                     | `20-alpine`          | `docker pull ghcr.io/loong64/node:20-alpine`             |
| [node](https://ghcr.io/loong64/node)                     | `20-trixie`          | `docker pull ghcr.io/loong64/node:20-trixie`             |
| [node](https://ghcr.io/loong64/node)                     | `20-trixie-slim`     | `docker pull ghcr.io/loong64/node:20-trixie-slim`        |
| [node](https://ghcr.io/loong64/node)                     | `22-alpine`          | `docker pull ghcr.io/loong64/node:22-alpine`             |
| [node](https://ghcr.io/loong64/node)                     | `22-trixie`          | `docker pull ghcr.io/loong64/node:22-trixie`             |
| [node](https://ghcr.io/loong64/node)                     | `22-trixie-slim`     | `docker pull ghcr.io/loong64/node:22-trixie-slim`        |
| [node](https://ghcr.io/loong64/node)                     | `23-alpine`          | `docker pull ghcr.io/loong64/node:23-alpine`             |
| [node](https://ghcr.io/loong64/node)                     | `23-trixie`          | `docker pull ghcr.io/loong64/node:23-trixie`             |
| [node](https://ghcr.io/loong64/node)                     | `23-trixie-slim`     | `docker pull ghcr.io/loong64/node:23-trixie-slim`        |
| [node](https://ghcr.io/loong64/node)                     | `24-alpine`          | `docker pull ghcr.io/loong64/node:24-alpine`             |
| [node](https://ghcr.io/loong64/node)                     | `24-trixie`          | `docker pull ghcr.io/loong64/node:24-trixie`             |
| [node](https://ghcr.io/loong64/node)                     | `24-trixie-slim`     | `docker pull ghcr.io/loong64/node:24-trixie-slim`        |
| [python](https://ghcr.io/loong64/python)                 | `3.9-alpine`         | `docker pull ghcr.io/loong64/python:3.9-alpine`          |
| [python](https://ghcr.io/loong64/python)                 | `3.9-trixie`         | `docker pull ghcr.io/loong64/python:3.9-trixie`          |
| [python](https://ghcr.io/loong64/python)                 | `3.9-slim-trixie`    | `docker pull ghcr.io/loong64/python:3.9-slim-trixie`     |
| [python](https://ghcr.io/loong64/python)                 | `3.10-alpine`        | `docker pull ghcr.io/loong64/python:3.10-alpine`         |
| [python](https://ghcr.io/loong64/python)                 | `3.10-trixie`        | `docker pull ghcr.io/loong64/python:3.10-trixie`         |
| [python](https://ghcr.io/loong64/python)                 | `3.10-slim-trixie`   | `docker pull ghcr.io/loong64/python:3.10-slim-trixie`    |
| [python](https://ghcr.io/loong64/python)                 | `3.11-alpine`        | `docker pull ghcr.io/loong64/python:3.11-alpine`         |
| [python](https://ghcr.io/loong64/python)                 | `3.11-trixie`        | `docker pull ghcr.io/loong64/python:3.11-trixie`         |
| [python](https://ghcr.io/loong64/python)                 | `3.11-slim-trixie`   | `docker pull ghcr.io/loong64/python:3.11-slim-trixie`    |
| [python](https://ghcr.io/loong64/python)                 | `3.12-alpine`        | `docker pull ghcr.io/loong64/python:3.12-alpine`         |
| [python](https://ghcr.io/loong64/python)                 | `3.12-trixie`        | `docker pull ghcr.io/loong64/python:3.12-trixie`         |
| [python](https://ghcr.io/loong64/python)                 | `3.12-slim-trixie`   | `docker pull ghcr.io/loong64/python:3.12-slim-trixie`    |
| [python](https://ghcr.io/loong64/python)                 | `3.13-alpine`        | `docker pull ghcr.io/loong64/python:3.13-alpine`         |
| [python](https://ghcr.io/loong64/python)                 | `3.13-trixie`        | `docker pull ghcr.io/loong64/python:3.13-trixie`         |
| [python](https://ghcr.io/loong64/python)                 | `3.13-slim-trixie`   | `docker pull ghcr.io/loong64/python:3.13-slim-trixie`    |
| [redis](https://ghcr.io/loong64/redis)                   | `7.2-alpine`         | `docker pull ghcr.io/loong64/redis:7.2-alpine`           |
| [redis](https://ghcr.io/loong64/redis)                   | `7.2-trixie`         | `docker pull ghcr.io/loong64/redis:7.2-trixie`           |
| [redis](https://ghcr.io/loong64/redis)                   | `7.4-alpine`         | `docker pull ghcr.io/loong64/redis:7.4-alpine`           |
| [redis](https://ghcr.io/loong64/redis)                   | `7.4-trixie`         | `docker pull ghcr.io/loong64/redis:7.4-trixie`           |
| [php](https://ghcr.io/loong64/php)                       | `8.1-cli-alpine3.21` | `docker pull ghcr.io/loong64/php:8.1-cli-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.1-fpm-alpine3.21` | `docker pull ghcr.io/loong64/php:8.1-fpm-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.1-zts-alpine3.21` | `docker pull ghcr.io/loong64/php:8.1-zts-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.2-cli-alpine3.21` | `docker pull ghcr.io/loong64/php:8.2-cli-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.2-fpm-alpine3.21` | `docker pull ghcr.io/loong64/php:8.2-fpm-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.2-zts-alpine3.21` | `docker pull ghcr.io/loong64/php:8.2-zts-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.3-cli-alpine3.21` | `docker pull ghcr.io/loong64/php:8.3-cli-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.3-fpm-alpine3.21` | `docker pull ghcr.io/loong64/php:8.3-fpm-alpine3.21`     |
| [php](https://ghcr.io/loong64/php)                       | `8.3-zts-alpine3.21` | `docker pull ghcr.io/loong64/php:8.3-zts-alpine3.21`     |
| [postgres](https://ghcr.io/loong64/postgres)             | `13-alpine`          | `docker pull ghcr.io/loong64/postgres:13-alpine`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `13-trixie`          | `docker pull ghcr.io/loong64/postgres:13-trixie`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `14-alpine`          | `docker pull ghcr.io/loong64/postgres:14-alpine`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `14-trixie`          | `docker pull ghcr.io/loong64/postgres:14-trixie`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `15-alpine`          | `docker pull ghcr.io/loong64/postgres:15-alpine`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `15-trixie`          | `docker pull ghcr.io/loong64/postgres:15-trixie`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `16-alpine`          | `docker pull ghcr.io/loong64/postgres:16-alpine`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `16-trixie`          | `docker pull ghcr.io/loong64/postgres:16-trixie`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `17-alpine`          | `docker pull ghcr.io/loong64/postgres:17-alpine`         |
| [postgres](https://ghcr.io/loong64/postgres)             | `17-trixie`          | `docker pull ghcr.io/loong64/postgres:17-trixie`         |
| [mariadb](https://ghcr.io/loong64/mariadb)               | `11.4`               | `docker pull ghcr.io/loong64/mariadb:11.4`               |
| [mariadb](https://ghcr.io/loong64/mariadb)               | `11.4-trixie`        | `docker pull ghcr.io/loong64/mariadb:11.4-trixie`        |
| [mariadb](https://ghcr.io/loong64/mariadb)               | `11.8-rc`            | `docker pull ghcr.io/loong64/mariadb:11.8-rc`            |
| [mariadb](https://ghcr.io/loong64/mariadb)               | `11.8-trixie-rc`     | `docker pull ghcr.io/loong64/mariadb:11.8-trixie-rc`     |
| [nginx](https://ghcr.io/loong64/nginx)                   | `1.26-alpine`        | `docker pull ghcr.io/loong64/nginx:1.26-alpine`          |
| [nginx](https://ghcr.io/loong64/nginx)                   | `1.26-trixie`        | `docker pull ghcr.io/loong64/nginx:1.26-trixie`          |
| [nginx](https://ghcr.io/loong64/nginx)                   | `1.27-alpine`        | `docker pull ghcr.io/loong64/nginx:1.27-alpine`          |
| [nginx](https://ghcr.io/loong64/nginx)                   | `1.27-trixie`        | `docker pull ghcr.io/loong64/nginx:1.27-trixie`          |
| [nginx](https://ghcr.io/loong64/nginx)                   | `1.28-alpine`        | `docker pull ghcr.io/loong64/nginx:1.28-alpine`          |
| [nginx](https://ghcr.io/loong64/nginx)                   | `1.28-trixie`        | `docker pull ghcr.io/loong64/nginx:1.28-trixie`          |
| [nextcloud](https://ghcr.io/loong64/nextcloud)           | `29-fpm-alpine`      | `docker pull ghcr.io/loong64/nextcloud:29-fpm-alpine`    |
| [nextcloud](https://ghcr.io/loong64/nextcloud)           | `30-fpm-alpine`      | `docker pull ghcr.io/loong64/nextcloud:30-fpm-alpine`    |
| [nextcloud](https://ghcr.io/loong64/nextcloud)           | `31-fpm-alpine`      | `docker pull ghcr.io/loong64/nextcloud:31-fpm-alpine`    |
| [n8n](https://ghcr.io/loong64/n8n)                       | `1.98.2`             | `docker pull ghcr.io/loong64/n8n:1.98.2`                 |
| [cloudreve](https://ghcr.io/loong64/cloudreve)           | `3.8.3`              | `docker pull ghcr.io/loong64/cloudreve:3.8.3`            |
| [cloudreve](https://ghcr.io/loong64/cloudreve)           | `4.0.0`              | `docker pull ghcr.io/loong64/cloudreve:4.0.0`            |
| [pgvector](https://ghcr.io/loong64/pgvector)             | `pg13`               | `docker pull ghcr.io/loong64/pgvector:pg13`              |
| [pgvector](https://ghcr.io/loong64/pgvector)             | `pg14`               | `docker pull ghcr.io/loong64/pgvector:pg14`              |
| [pgvector](https://ghcr.io/loong64/pgvector)             | `pg15`               | `docker pull ghcr.io/loong64/pgvector:pg15`              |
| [pgvector](https://ghcr.io/loong64/pgvector)             | `pg16`               | `docker pull ghcr.io/loong64/pgvector:pg16`              |
| [pgvector](https://ghcr.io/loong64/pgvector)             | `pg17`               | `docker pull ghcr.io/loong64/pgvector:pg17`              |
| [openlist](https://ghcr.io/loong64/openlist)             | `v4.0.0`             | `docker pull ghcr.io/loong64/openlist:v4.0.0`            |

</details>

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

Python Package Index. **[pypi](https://gitlab.com/loong64/pypi/-/packages/)**

```sh
# pip install "SomeProject" --extra-index-url https://mirrors.loong64.com/pypi/simple
pip install poetry --extra-index-url https://mirrors.loong64.com/pypi/simple
```

<details>

<summary>Details ...</summary>

----
The Python Package Index

- https://mirrors.loong64.com/pypi/simple
- https://gitlab.com/api/v4/projects/65746188/packages/pypi/simple

| Name                 | Install Command                                                               |
| -------------------- | ----------------------------------------------------------------------------- |
| aiohttp              | `pip install aiohttp -i https://mirrors.loong64.com/pypi/simple`              |
| argon2-cffi-bindings | `pip install argon2-cffi-bindings -i https://mirrors.loong64.com/pypi/simple` |
| auditwheel           | `pip install auditwheel -i https://mirrors.loong64.com/pypi/simple`           |
| bcrypt               | `pip install bcrypt -i https://mirrors.loong64.com/pypi/simple`               |
| cffi                 | `pip install cffi -i https://mirrors.loong64.com/pypi/simple`                 |
| cmake                | `pip install cmake -i https://mirrors.loong64.com/pypi/simple`                |
| contourpy            | `pip install contourpy -i https://mirrors.loong64.com/pypi/simple`            |
| cryptography         | `pip install cryptography -i https://mirrors.loong64.com/pypi/simple`         |
| gevent               | `pip install gevent -i https://mirrors.loong64.com/pypi/simple`               |
| ephem                | `pip install ephem -i https://mirrors.loong64.com/pypi/simple`                |
| gmpy2                | `pip install gmpy2 -i https://mirrors.loong64.com/pypi/simple`                |
| greenlet             | `pip install greenlet -i https://mirrors.loong64.com/pypi/simple`             |
| grpcio               | `pip install grpcio -i https://mirrors.loong64.com/pypi/simple`               |
| h5py                 | `pip install h5py -i https://mirrors.loong64.com/pypi/simple`                 |
| httptools            | `pip install httptools  -i https://mirrors.loong64.com/pypi/simple`           |
| insightface          | `pip install insightface -i https://mirrors.loong64.com/pypi/simple`          |
| jiter                | `pip install jiter -i https://mirrors.loong64.com/pypi/simple`                |
| Levenshtein          | `pip install Levenshtein -i https://mirrors.loong64.com/pypi/simple`          |
| lxml                 | `pip install lxml -i https://mirrors.loong64.com/pypi/simple`                 |
| MarkupSafe           | `pip install MarkupSafe -i https://mirrors.loong64.com/pypi/simple`           |
| matplotlib           | `pip install matplotlib -i https://mirrors.loong64.com/pypi/simple`           |
| maxminddb            | `pip install maxminddb -i https://mirrors.loong64.com/pypi/simple`            |
| maturin              | `pip install maturin -i https://mirrors.loong64.com/pypi/simple`              |
| msgpack              | `pip install msgpack -i https://mirrors.loong64.com/pypi/simple`              |
| netifaces            | `pip install netifaces -i https://mirrors.loong64.com/pypi/simple`            |
| nh3                  | `pip install nh3 -i https://mirrors.loong64.com/pypi/simple`                  |
| ninja                | `pip install ninja -i https://mirrors.loong64.com/pypi/simple`                |
| numpy                | `pip install numpy -i https://mirrors.loong64.com/pypi/simple`                |
| ml-dtypes            | `pip install ml-dtypes -i https://mirrors.loong64.com/pypi/simple`            |
| mysqlclient          | `pip install mysqlclient -i https://mirrors.loong64.com/pypi/simple`          |
| torch                | `pip install torch -i https://mirrors.loong64.com/pypi/simple`                |
| torchaudio           | `pip install torchaudio -i https://mirrors.loong64.com/pypi/simple`           |
| torchvision          | `pip install torchvision -i https://mirrors.loong64.com/pypi/simple`          |
| onnx                 | `pip install onnx -i https://mirrors.loong64.com/pypi/simple`                 |
| onnxruntime          | `pip install onnxruntime -i https://mirrors.loong64.com/pypi/simple`          |
| opencv-python        | `pip install opencv-python -i https://mirrors.loong64.com/pypi/simple`        |
| optree               | `pip install optree -i https://mirrors.loong64.com/pypi/simple`               |
| oracledb             | `pip install oracledb -i https://mirrors.loong64.com/pypi/simple`             |
| orjson               | `pip install orjson -i https://mirrors.loong64.com/pypi/simple`               |
| pandas               | `pip install pandas -i https://mirrors.loong64.com/pypi/simple`               |
| patchelf             | `pip install patchelf  -i https://mirrors.loong64.com/pypi/simple`            |
| pillow               | `pip install pillow -i https://mirrors.loong64.com/pypi/simple`               |
| psutil               | `pip install psutil -i https://mirrors.loong64.com/pypi/simple`               |
| psycopg2-binary      | `pip install psycopg2-binary -i https://mirrors.loong64.com/pypi/simple`      |
| pycryptodome         | `pip install pycryptodome -i https://mirrors.loong64.com/pypi/simple`         |
| pycryptodomex        | `pip install pycryptodomex -i https://mirrors.loong64.com/pypi/simple`        |
| pydantic-core        | `pip install pydantic-core -i https://mirrors.loong64.com/pypi/simple`        |
| pymongo              | `pip install pymongo -i https://mirrors.loong64.com/pypi/simple`              |
| PyNaCl               | `pip install PyNaCl -i https://mirrors.loong64.com/pypi/simple`               |
| PyYAML               | `pip install PyYAML -i https://mirrors.loong64.com/pypi/simple`               |
| pyzmq                | `pip install pyzmq -i https://mirrors.loong64.com/pypi/simple`                |
| scikit-image         | `pip install scikit-image -i https://mirrors.loong64.com/pypi/simple`         |
| scikit-learn         | `pip install scikit-learn -i https://mirrors.loong64.com/pypi/simple`         |
| scipy-openblas32     | `pip install scipy-openblas32 -i https://mirrors.loong64.com/pypi/simple`     |
| scipy-openblas64     | `pip install scipy-openblas64 -i https://mirrors.loong64.com/pypi/simple`     |
| sentencepiece        | `pip install sentencepiece -i https://mirrors.loong64.com/pypi/simple`        |
| shapely              | `pip install shapely -i https://mirrors.loong64.com/pypi/simple`              |
| simsimd              | `pip install simsimd -i https://mirrors.loong64.com/pypi/simple`              |
| stringzilla          | `pip install stringzilla -i https://mirrors.loong64.com/pypi/simple`          |
| swig                 | `pip install swig -i https://mirrors.loong64.com/pypi/simple`                 |
| tokenizers           | `pip install tokenizers -i https://mirrors.loong64.com/pypi/simple`           |
| tornado              | `pip install tornado -i https://mirrors.loong64.com/pypi/simple`              |
| xmlsec               | `pip install xmlsec -i https://mirrors.loong64.com/pypi/simple`               |
| uv                   | `pip install uv -i https://mirrors.loong64.com/pypi/simple`                   |
| uvloop               | `pip install uvloop -i https://mirrors.loong64.com/pypi/simple`               |
| watchfiles           | `pip install watchfiles -i https://mirrors.loong64.com/pypi/simple`           |
| zope.interface       | `pip install zope.interface -i https://mirrors.loong64.com/pypi/simple`       |
| zstandard            | `pip install zstandard -i https://mirrors.loong64.com/pypi/simple`            |

Built Packages on **[manylinux](https://github.com/loong64/manylinux)** and **[manylinux-cross](https://github.com/loong64/manylinux-cross)**

| Name                                                                             | Tag            | Pull Command                                                          |
| -------------------------------------------------------------------------------- | -------------- | --------------------------------------------------------------------- |
| [manylinux_2_36-cross](https://ghcr.io/loong64/manylinux_2_36-cross)             | `loongarch64`  | `docker pull ghcr.io/loong64/manylinux_2_36-cross:loongarch64`        |
| [manylinux_2_38_loongarch64](https://ghcr.io/loong64/manylinux_2_38_loongarch64) | `2025.05.18-0` | `docker pull ghcr.io/loong64/manylinux_2_38_loongarch64:2025.05.18-0` |
| [musllinux_1_2-cross](https://ghcr.io/loong64/musllinux_1_2-cross)               | `loongarch64`  | `docker pull ghcr.io/loong64/musllinux_1_2-cross:loongarch64`         |
| [musllinux_1_2_loongarch64](https://ghcr.io/loong64/musllinux_1_2_loongarch64)   | `2025.05.18-0` | `docker pull ghcr.io/loong64/musllinux_1_2_loongarch64:2025.05.18-0`  |

</details>

More packages will be added ...

## Links

<a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=XZj-dzRYq2BTQ_SulR3VHZ0dLO1XI7ek&jump_from=webapi&authKey=+DqUmM7wBsAOTWNI6+zu0ZCyIgav4WUu4evgRJAqvakDOr9iB4paFolaE0fWDiq2"><img border="0" src="https://pub.idqqimg.com/wpa/images/group.png" alt="LoongArch64 开源交流群" title="LoongArch64 开源交流群"></a>