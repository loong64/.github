<h3 align="center">The <a href="https://wiki.debian.org/LoongArch">LoongArch</a> architecture is a RISC-style ISA developed by <a href="https://www.loongson.cn/">Loongson</a> <br> LoongArch64 is the 64-bit version of <a href="https://wiki.debian.org/LoongArch">LoongArch</a></h3>

------------------------------

## Quick Start

| OS/Arch         | Arch      | Architecture   |
| --------------- | --------- | -------------- |
| `linux/loong64` | `loong64` | `loongarch64`  |

You can use **[Docker](https://docs.docker.com/get-started/get-docker/)** to quickly deploy.

```bash
docker run --rm --privileged ghcr.io/loong64/qemu-user-static --reset -p yes
docker run --rm -it ghcr.io/loong64/debian:trixie-slim bash
```

Or use **[Debian CD](https://cdimage.debian.org/cdimage/ports/snapshots/2024-11-11/)** to boot.

| Name                                                                                                                                     | Description                                                         |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [debian-12.0.0-loong64-NETINST-1.iso](https://cdimage.debian.org/cdimage/ports/tests/loong64-test-20241115-2/debian-12.0.0-loong64-NETINST-1.iso) | contains installer images for the non-release "ports" architectures |

## Applications

Binary applications.

| Name                                                                   | Release                                                                                                                                                         | Description                            |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Node.js](https://github.com/loong64/node/releases)                    | <a href="https://github.com/loong64/node/releases"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/node.svg"/></a>                        | Node.js JavaScript runtime ✨🐢🚀✨  |
| [Docker](https://github.com/loong64/docker-ce-packaging/releases)      | <a href="https://github.com/loong64/docker-ce-packaging"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/docker-ce-packaging.svg"/></a>   | Packaging scripts for Docker CE        |
| [Containerd](https://github.com/loong64/containerd-packaging/releases) | <a href="https://github.com/loong64/containerd-packaging"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/containerd-packaging.svg"/></a> | Linux distro packaging for containerd  |

## Docker Images

GitHub Container Registry. Images are built on **[docker-library](https://github.com/loong64/docker-library)**

| Name                                                                                      | Tag                | Pull Command                                             |
| ----------------------------------------------------------------------------------------- | ------------------ | -------------------------------------------------------- |
| [debian](https://github.com/loong64/docker-debian-build/pkgs/container/debian)            | `trixie`           | `docker pull ghcr.io/loong64/debian:trixie`              |
| [debian](https://github.com/loong64/docker-debian-build/pkgs/container/debian)            | `trixie-slim`      | `docker pull ghcr.io/loong64/debian:trixie-slim`         |
| [buildpack-deps](https://github.com/loong64/docker-library/pkgs/container/buildpack-deps) | `trixie`           | `docker pull ghcr.io/loong64/buildpack-deps:trixie`      |
| [buildpack-deps](https://github.com/loong64/docker-library/pkgs/container/buildpack-deps) | `trixie-scm`       | `docker pull ghcr.io/loong64/buildpack-deps:trixie-scm`  |
| [buildpack-deps](https://github.com/loong64/docker-library/pkgs/container/buildpack-deps) | `trixie-curl`      | `docker pull ghcr.io/loong64/buildpack-deps:trixie-curl` |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.21-trixie`      | `docker pull ghcr.io/loong64/golang:1.21-trixie`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.22-trixie`      | `docker pull ghcr.io/loong64/golang:1.22-trixie`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.23-trixie`      | `docker pull ghcr.io/loong64/golang:1.23-trixie`         |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `18-trixie`        | `docker pull ghcr.io/loong64/node:18-trixie`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `18-trixie-slim`   | `docker pull ghcr.io/loong64/node:18-trixie-slim`        |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `20-trixie`        | `docker pull ghcr.io/loong64/node:20-trixie`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `20-trixie-slim`   | `docker pull ghcr.io/loong64/node:20-trixie-slim`        |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.9-trixie`       | `docker pull ghcr.io/loong64/python:3.9-trixie`          |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.9-slim-trixie`  | `docker pull ghcr.io/loong64/python:3.9-slim-trixie`     |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.10-trixie`      | `docker pull ghcr.io/loong64/python:3.10-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.10-slim-trixie` | `docker pull ghcr.io/loong64/python:3.10-slim-trixie`    |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.11-trixie`      | `docker pull ghcr.io/loong64/python:3.11-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.11-slim-trixie` | `docker pull ghcr.io/loong64/python:3.11-slim-trixie`    |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.12-trixie`      | `docker pull ghcr.io/loong64/python:3.12-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.12-slim-trixie` | `docker pull ghcr.io/loong64/python:3.12-slim-trixie`    |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.13-trixie`      | `docker pull ghcr.io/loong64/python:3.13-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.13-slim-trixie` | `docker pull ghcr.io/loong64/python:3.13-slim-trixie`    |