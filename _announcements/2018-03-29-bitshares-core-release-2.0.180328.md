---
title: BitShares Core Release 2.0.180328
layout: announcement
---

The BitShares Blockchain Foundation is thrilled to announce a new release of
the BitShares Core software by the core developers.

**This release contains several security fixes. All nodes please upgrade as soon as possible.**

## How to upgrade
```
git fetch origin
git checkout 2.0.180328
git submodule update --init --recursive  # this command will fail
git submodule sync --recursive
git submodule update --init --recursive

# it follows the usual compile instructions with cmake and make
```

Furthermore, an additional dependency for `libcurl` has been added and required
you to install the development package:

    apt-get install libcurl4-openssl-dev

## Change Log

The detailed lists about bug and security fixes can be found in the [Release
Notes](https://github.com/bitshares/bitshares-core/releases/tag/2.0.180328).

## Docker

The new docker container has been built by Docker Hub and is available via

    docker pull bitshares/bitshares-core:2.0.180328
