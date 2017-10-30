---
title: BitShares Core Release 2.0.171025
layout: announcement
---

The BitShares Blockchain Foundation is happy to announce a [new
release](https://github.com/bitshares/bitshares-core/releases/tag/2.0.171025)
of the BitShares core backend. After **three months** of hard work by
the backend developers, release
[2.0.171025](https://github.com/bitshares/bitshares-core/releases/tag/2.0.171025)
was tagged.

**This is a consensus changing protocol upgrade**

All full nodes must upgrade before **2017-11-27 14:40:00 UTC**!

# Content
* TOC
{:toc}

## Major Changes

* [BSIP-0018](https://github.com/bitshares/bitshares-core/pull/340):
  This is a consensus changing modification that implements [BSIP-0018](https://github.com/bitshares/bsips/blob/master/bsip-0018.md) - *Revive BitAsset through buying Settlement Pool*. The modification will allow for every BitShares holder to (partially) bid for the collateral position after a global settlement of a bitasset.
* [new option --plugins for run-time selection of active plugins](https://github.com/bitshares/bitshares-core/pull/288): The `plugins` configuration allows to enable those plugins that are supported by the node. This greatly simplifies the configuration and allows to run reduced RAM nodes easily.
* Some API changes [#352](https://github.com/bitshares/bitshares-core/pull/#352) [#344](https://github.com/bitshares/bitshares-core/pull/#344) [#347](https://github.com/bitshares/bitshares-core/pull/#347) [#330](https://github.com/bitshares/bitshares-core/pull/#330) [#311](https://github.com/bitshares/bitshares-core/pull/#311) [#312](https://github.com/bitshares/bitshares-core/pull/#312) [#306](https://github.com/bitshares/bitshares-core/pull/#306) [#304](https://github.com/bitshares/bitshares-core/pull/#304) [#420](https://github.com/bitshares/bitshares-core/pull/#420): Most of these modifications simplify the usage of the interface to gain access to the blockchain database, others add new functionality (calls).

## Performance Changes

* [Improved startup time](https://github.com/bitshares/bitshares-core/pull/339): This change will greatly improve startup time for nodes.
* [Incorporate p2p fixes that were made to steem codebase](https://github.com/bitshares/bitshares-core/issues/411): This patch adds the improvements made by Steemit Inc. to BitShares. It resolves that P2P connections would get stuck sometimes, which would lead to the network seeming to be stuck.
* [Changed default settings to reduce RAM for new nodes](https://github.com/bitshares/bitshares-core/pull/422): If no configuration file has been created already, the default configuration will ensure that only up to 1000 elements are stored in the history of each account and by this drastically reduces the RAM usage of the BitShares core.


## Minor Fixes
* [Fix for bug in vote evaluation](https://github.com/bitshares/bitshares-core/pull/369)
* [Fix to prohibit voting for non-existant entities](https://github.com/bitshares/bitshares-core/pull/348)
* [Fix for the "no blocks to pop" message during shutdown](https://github.com/bitshares/bitshares-core/pull/336)
* [Fix for transaction signing in cli_wallet](https://github.com/bitshares/bitshares-core/pull/321)
* [Improved error logging](https://github.com/bitshares/bitshares-core/pull/332)
* [Get rid of broken flat_index](https://github.com/bitshares/bitshares-core/pull/335)
* [Fixed rounding issue when creating assets](https://github.com/bitshares/bitshares-core/issues/429)
* [Fix and softfork protection for asset creation fee issue](https://github.com/bitshares/bitshares-core/issues/433)
* [Fixed issue of more than 100 accounts owned by the same user](https://github.com/bitshares/bitshares-core/issues/295)
* [Prevent new bid_collateral operation from entering the blockchain before hardfork](https://github.com/bitshares/bitshares-core/pull/441)
* [Fix for early withdrawal claims](https://github.com/bitshares/bitshares-core/pull/386)

## Protocol Upgrade: A reliable and secure hard fork

The new release modifies the blockchain protocol (by adding BSIP18) and
due to this is a consensus-changing modification. While the usual
terminology for this kind of upgrade in other blockchains is
**hard-fork**, we would like to emphasis a new term for Graphene-based
blockchains: **protocol upgrade**. The reasons we distinguish our
upgrades from a **hard-forks**, is that our consensus mechanism -
delegated proof of stake (DPOS) - does **not allow** for the blockchain
to **split** into two (or even more) independent blockchains.
BitShares comes with an **inherent replay protection** and together with
BTS holder-approved block producers cannot result in a splitting of the
blockchain.
