---
title: BitShares Core Release 2.0.180823 (optional upgrade)
layout: announcement
---

The BitShares Blockchain Foundation is pleased to inform the community about
the latest feature release for the [BitShares main
network](https://wallet.bitshares.org/).

After many weeks of development and over two weeks testing on the [bitshares
testnet](https://testnet.bitshares.eu/), this final version

    2.0.180823

has been tagged in the [bitshares-core](https://github.com/bitshares/bitshares-core/releases) repository on GitHub.

**Important remark:** This is a __feature release__ adding support for Ubuntu
18.04 LTS and numerous security enhancements. Validation nodes are encouraged
to upgrade (will replay automatically on first run).

## Release Highlights

- [Added](https://github.com/bitshares/bitshares-core/issues/835) Openssl 1.1 and Ubuntu 18.04 support
- [Improved](https://github.com/bitshares/bitshares-core/issues/1103) Elasticsearch performance and functionality (see: [documentation](https://github.com/bitshares/bitshares-core/wiki/ElasticSearch-Plugin))
- [Fixed](https://github.com/bitshares/bitshares-core/releases) 8 bugs
- [Added](https://github.com/bitshares/bitshares-core/releases) multiple API enhancements for improved queries and return data
- [Improved] Docker support

**[Complete Release Notes(https://github.com/bitshares/bitshares-core/releases)]**

## How to upgrade from sources

    cd bitshares-core
    git fetch origin
    git checkout 2.0.180823
    git submodule sync --recursive
    git submodule update --init --recursive

Follow the usual compile instructions with cmake and make

## Change Log

The detailed lists of updates, bug fixes and security fixes can be found in the
Release Notes(https://github.com/bitshares/bitshares-core/releases)]

## Docker

The new docker container has been built by Docker Hub and is available via

    docker pull bitshares/bitshares-core:2.0.180823

## Feature Release

This new release enhances the platform functionality without modifying the
underlying consensus protocol.
