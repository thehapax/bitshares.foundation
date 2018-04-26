---
title: BitShares Core Release 2.0.180425
layout: announcement
---

The BitShares Blockchain Foundation is thrilled to announce a new release of
the BitShares Core software by the core developers.

**This is a bugfix release.**

## How to upgrade
```
git fetch origin
git checkout 2.0.180425
git submodule sync --recursive
git submodule update --init --recursive

# it follows the usual compile instructions with cmake and make
```

## Change Log

The detailed lists about bug and security fixes can be found in the [Release
Notes](https://github.com/bitshares/bitshares-core/releases/tag/2.0.180425)

## Docker

The new docker container has been built by Docker Hub and is available via

    docker pull bitshares/bitshares-core:2.0.180425
