[![Docker pulls](https://img.shields.io/docker/pulls/dlanguage/sdc.svg)](https://hub.docker.com/r/dlanguage/sdc/)
[![Docker Build](https://img.shields.io/docker/automated/dlanguage/sdc.svg)](https://hub.docker.com/r/dlanguage/sdc/)
[![Latest Tag](https://img.shields.io/github/tag/lindt/docker-sdc.svg)](https://hub.docker.com/r/dlanguage/sdc/)

# docker-sdc

Docker Image for Stupid D Compiler [SDC](https://github.com/SDC-Developers/SDC).

## Motivation

Installation of a compiler sometimes is cumbersome. This Docker image should take this pain and allow you to easily switch between Versions of the same compiler and even different compilers.

The SDC is still hasn't reached version 1.0.
It could just compile basic stuff.
To see what it's able to compile, check out it's [tests](https://github.com/SDC-Developers/SDC/tree/master/tests).

## Other Compilers

Allows to use all major D Compilers without installation.

| Compiler | Latest Tag |
| -------- | ---------- |
| DMD      | [![Latest Tag](https://img.shields.io/github/tag/lindt/docker-dmd.svg)](https://hub.docker.com/r/dlanguage/dmd/) |
| LDC      | [![Latest Tag](https://img.shields.io/github/tag/lindt/docker-ldc.svg)](https://hub.docker.com/r/dlanguage/ldc/) |
| GDC      | [![Latest Tag](https://img.shields.io/github/tag/lindt/docker-gdc.svg)](https://hub.docker.com/r/dlanguage/gdc/) |
| SDC      | [![Latest Tag](https://img.shields.io/github/tag/lindt/docker-sdc.svg)](https://hub.docker.com/r/dlanguage/sdc/) |

## Usage

Place a `test.d` in your current directory.
Then execute
```
docker run --rm -ti \
  -e USER -e HOME -e LOCAL_USER_ID=`id -u $USER` -e LOCAL_GROUP_ID=`id -g $USER` \
  -w /src \
  -v $(pwd):/src \
  dlanguage/sdc sdc test.d
```
