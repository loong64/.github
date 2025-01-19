<h3 align="center">The <a href="https://wiki.debian.org/LoongArch">LoongArch</a> architecture is a RISC-style ISA developed by <a href="https://www.loongson.cn/">Loongson</a> <br> LoongArch64 is the 64-bit version of <a href="https://wiki.debian.org/LoongArch">LoongArch</a></h3>

------------------------------

## Quick Start

| OS/Arch         | Arch      | Architecture   |
| --------------- | --------- | -------------- |
| `linux/loong64` | `loong64` | `loongarch64`  |

You can use **[Docker](https://docs.docker.com/get-started/get-docker/)** to quickly deploy.

```bash
# Set up QEMU
docker run --rm --privileged ghcr.io/loong64/qemu-user-static --reset -p yes

# Alpine
docker run --rm --platform linux/loong64 -it ghcr.io/loong64/alpine:3.21 sh

# Debian
docker run --rm --platform linux/loong64 -it ghcr.io/loong64/debian:trixie-slim bash
```

Or use Linux OS to boot.

- **[Alpine Linux](https://www.alpinelinux.org/downloads/)** 
- **[Debian GNU/Linux](https://cdimage.debian.org/cdimage/ports/snapshots/2024-12-24/)** 

| Name                                                                                                                                              | Description                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| [alpine-standard-3.21.2-loongarch64.iso](https://dl-cdn.alpinelinux.org/alpine/v3.21/releases/loongarch64/alpine-standard-3.21.2-loongarch64.iso) | Alpine as it was intended. Just enough to get you started.           |
| [debian-12.0.0-loong64-NETINST-1.iso](https://cdimage.debian.org/cdimage/ports/snapshots/2024-12-24/debian-12.0.0-loong64-NETINST-1.iso)          | contains installer images for the non-release "ports" architectures. |

## Applications

Binary applications.

| Name                                                                   | Release                                                                                                                                                         | Description                            |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [Node.js](https://github.com/loong64/node/releases)                    | <a href="https://github.com/loong64/node/releases"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/node.svg"/></a>                        | Node.js JavaScript runtime ✨🐢🚀✨  |
| [Docker](https://github.com/loong64/docker-ce-packaging/releases)      | <a href="https://github.com/loong64/docker-ce-packaging"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/docker-ce-packaging.svg"/></a>   | Packaging scripts for Docker CE        |
| [Containerd](https://github.com/loong64/containerd-packaging/releases) | <a href="https://github.com/loong64/containerd-packaging"><img alt="Node.js" src="https://img.shields.io/github/release/loong64/containerd-packaging.svg"/></a> | Linux distro packaging for containerd  |

## Docker Images

GitHub Container Registry. Images are built on **[docker-library](https://github.com/loong64/docker-library)**

<details>

<summary>Details ...</summary>

----

| Name                                                                                      | Tag                | Pull Command                                             |
| ----------------------------------------------------------------------------------------- | ------------------ | -------------------------------------------------------- |
| [alpine](https://github.com/loong64/docker-debian-build/pkgs/container/alpine)            | `3.21`             | `docker pull ghcr.io/loong64/alpine:3.21`                |
| [debian](https://github.com/loong64/docker-debian-build/pkgs/container/debian)            | `trixie`           | `docker pull ghcr.io/loong64/debian:trixie`              |
| [debian](https://github.com/loong64/docker-debian-build/pkgs/container/debian)            | `trixie-slim`      | `docker pull ghcr.io/loong64/debian:trixie-slim`         |
| [buildpack-deps](https://github.com/loong64/docker-library/pkgs/container/buildpack-deps) | `trixie`           | `docker pull ghcr.io/loong64/buildpack-deps:trixie`      |
| [buildpack-deps](https://github.com/loong64/docker-library/pkgs/container/buildpack-deps) | `trixie-scm`       | `docker pull ghcr.io/loong64/buildpack-deps:trixie-scm`  |
| [buildpack-deps](https://github.com/loong64/docker-library/pkgs/container/buildpack-deps) | `trixie-curl`      | `docker pull ghcr.io/loong64/buildpack-deps:trixie-curl` |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.21-alpine`      | `docker pull ghcr.io/loong64/golang:1.21-alpine`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.21-trixie`      | `docker pull ghcr.io/loong64/golang:1.21-trixie`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.22-alpine`      | `docker pull ghcr.io/loong64/golang:1.22-alpine`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.22-trixie`      | `docker pull ghcr.io/loong64/golang:1.22-trixie`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.23-alpine`      | `docker pull ghcr.io/loong64/golang:1.23-alpine`         |
| [golang](https://github.com/loong64/docker-library/pkgs/container/golang)                 | `1.23-trixie`      | `docker pull ghcr.io/loong64/golang:1.23-trixie`         |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `18-alpine`        | `docker pull ghcr.io/loong64/node:18-alpine`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `18-trixie`        | `docker pull ghcr.io/loong64/node:18-trixie`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `18-trixie-slim`   | `docker pull ghcr.io/loong64/node:18-trixie-slim`        |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `20-alpine`        | `docker pull ghcr.io/loong64/node:20-alpine`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `20-trixie`        | `docker pull ghcr.io/loong64/node:20-trixie`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `20-trixie-slim`   | `docker pull ghcr.io/loong64/node:20-trixie-slim`        |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `22-alpine`        | `docker pull ghcr.io/loong64/node:22-alpine`             |
| [node](https://github.com/loong64/docker-library/pkgs/container/node)                     | `23-alpine`        | `docker pull ghcr.io/loong64/node:23-alpine`             |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.9-alpine`       | `docker pull ghcr.io/loong64/python:3.9-alpine`          |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.9-trixie`       | `docker pull ghcr.io/loong64/python:3.9-trixie`          |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.9-slim-trixie`  | `docker pull ghcr.io/loong64/python:3.9-slim-trixie`     |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.10-alpine`      | `docker pull ghcr.io/loong64/python:3.10-alpine`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.10-trixie`      | `docker pull ghcr.io/loong64/python:3.10-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.10-slim-trixie` | `docker pull ghcr.io/loong64/python:3.10-slim-trixie`    |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.11-alpine`      | `docker pull ghcr.io/loong64/python:3.11-alpine`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.11-trixie`      | `docker pull ghcr.io/loong64/python:3.11-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.11-slim-trixie` | `docker pull ghcr.io/loong64/python:3.11-slim-trixie`    |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.12-alpine`      | `docker pull ghcr.io/loong64/python:3.12-alpine`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.12-trixie`      | `docker pull ghcr.io/loong64/python:3.12-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.12-slim-trixie` | `docker pull ghcr.io/loong64/python:3.12-slim-trixie`    |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.13-alpine`      | `docker pull ghcr.io/loong64/python:3.13-alpine`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.13-trixie`      | `docker pull ghcr.io/loong64/python:3.13-trixie`         |
| [python](https://github.com/loong64/docker-library/pkgs/container/python)                 | `3.13-slim-trixie` | `docker pull ghcr.io/loong64/python:3.13-slim-trixie`    |

</details>

More Docker images will be added ...

## Docker Repository

Install Docker Engine on Debian. **[Packages](https://github.com/loong64/repo)**

```sh
# Add Docker's official GPG key:
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

## PyPI Repository

Python Package Index. **[PyPI](https://gitlab.com/loong64/pypi/-/packages/)**

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

| Name                 | Install Command                                                             |
| -------------------- | --------------------------------------------------------------------------- |
| aiohttp              | pip install aiohttp -i https://mirrors.loong64.com/pypi/simple              |
| argon2-cffi-bindings | pip install argon2-cffi-bindings -i https://mirrors.loong64.com/pypi/simple |
| auditwheel           | pip install auditwheel -i https://mirrors.loong64.com/pypi/simple           |
| bcrypt               | pip install bcrypt -i https://mirrors.loong64.com/pypi/simple               |
| cffi                 | pip install cffi -i https://mirrors.loong64.com/pypi/simple                 |
| cmake                | pip install cmake -i https://mirrors.loong64.com/pypi/simple                |
| contourpy            | pip install contourpy -i https://mirrors.loong64.com/pypi/simple            |
| cryptography         | pip install cryptography -i https://mirrors.loong64.com/pypi/simple         |
| ephem                | pip install ephem -i https://mirrors.loong64.com/pypi/simple                |
| greenlet             | pip install greenlet -i https://mirrors.loong64.com/pypi/simple             |
| grpcio               | pip install grpcio -i https://mirrors.loong64.com/pypi/simple               |
| jiter                | pip install jiter -i https://mirrors.loong64.com/pypi/simple                |
| lxml                 | pip install lxml -i https://mirrors.loong64.com/pypi/simple                 |
| MarkupSafe           | pip install MarkupSafe -i https://mirrors.loong64.com/pypi/simple           |
| matplotlib           | pip install matplotlib -i https://mirrors.loong64.com/pypi/simple           |
| maxminddb            | pip install maxminddb -i https://mirrors.loong64.com/pypi/simple            |
| maturin              | pip install maturin -i https://mirrors.loong64.com/pypi/simple              |
| msgpack              | pip install msgpack -i https://mirrors.loong64.com/pypi/simple              |
| netifaces            | pip install netifaces -i https://mirrors.loong64.com/pypi/simple            |
| nh3                  | pip install nh3 -i https://mirrors.loong64.com/pypi/simple                  |
| ninja                | pip install ninja -i https://mirrors.loong64.com/pypi/simple                |
| numpy                | pip install numpy -i https://mirrors.loong64.com/pypi/simple                |
| mysqlclient          | pip install mysqlclient -i https://mirrors.loong64.com/pypi/simple          |
| onnx                 | pip install onnx -i https://mirrors.loong64.com/pypi/simple                 |
| opencv-python        | pip install opencv-python -i https://mirrors.loong64.com/pypi/simple        |
| optree               | pip install optree -i https://mirrors.loong64.com/pypi/simple               |
| oracledb             | pip install oracledb -i https://mirrors.loong64.com/pypi/simple             |
| pandas               | pip install pandas -i https://mirrors.loong64.com/pypi/simple               |
| patchelf             | pip install patchelf  -i https://mirrors.loong64.com/pypi/simple            |
| pillow               | pip install pillow -i https://mirrors.loong64.com/pypi/simple               |
| psutil               | pip install psutil -i https://mirrors.loong64.com/pypi/simple               |
| psycopg2-binary      | pip install psycopg2-binary -i https://mirrors.loong64.com/pypi/simple      |
| pycryptodome         | pip install pycryptodome -i https://mirrors.loong64.com/pypi/simple         |
| pycryptodomex        | pip install pycryptodomex -i https://mirrors.loong64.com/pypi/simple        |
| pydantic-core        | pip install pydantic-core -i https://mirrors.loong64.com/pypi/simple        |
| pymongo              | pip install pymongo -i https://mirrors.loong64.com/pypi/simple              |
| PyNaCl               | pip install PyNaCl -i https://mirrors.loong64.com/pypi/simple               |
| PyYAML               | pip install PyYAML -i https://mirrors.loong64.com/pypi/simple               |
| pyzmq                | pip install pyzmq -i https://mirrors.loong64.com/pypi/simple                |
| scipy-openblas32     | pip install scipy-openblas32 -i https://mirrors.loong64.com/pypi/simple     |
| scipy-openblas64     | pip install scipy-openblas64 -i https://mirrors.loong64.com/pypi/simple     |
| sentencepiece        | pip install sentencepiece -i https://mirrors.loong64.com/pypi/simple        |
| swig                 | pip install swig -i https://mirrors.loong64.com/pypi/simple                 |
| tornado              | pip install tornado -i https://mirrors.loong64.com/pypi/simple              |
| xmlsec               | pip install xmlsec -i https://mirrors.loong64.com/pypi/simple               |
| uv                   | pip install uv -i https://mirrors.loong64.com/pypi/simple                   |
| zope.interface       | pip install zope.interface -i https://mirrors.loong64.com/pypi/simple       |

Built Packages on **[manylinux](https://github.com/loong64/manylinux)**

| Name                                                                                                         | Tag            | Pull Command                                                          |
| ------------------------------------------------------------------------------------------------------------ | -------------- | --------------------------------------------------------------------- |
| [manylinux_2_38_loongarch64](https://github.com/loong64/manylinux/pkgs/container/manylinux_2_38_loongarch64) | `2024.12.31-1` | `docker pull ghcr.io/loong64/manylinux_2_38_loongarch64:2024.12.31-1` |
| [manylinux_2_38_loongarch64](https://github.com/loong64/manylinux/pkgs/container/manylinux_2_38_loongarch64) | `2025.01.07-1` | `docker pull ghcr.io/loong64/manylinux_2_38_loongarch64:2025.01.07-1` |
| [manylinux_2_38_loongarch64](https://github.com/loong64/manylinux/pkgs/container/manylinux_2_38_loongarch64) | `2025.01.16-1` | `docker pull ghcr.io/loong64/manylinux_2_38_loongarch64:2025.01.16-1` |

</details>

More packages will be added ...