---
title: BitShares Block Production Incident Report
layout: announcement
---

On Monday, July 10th 2017 at 8:30am UTC, an incident occurred on the BitShares
network that caused an unplanned interruption of block production. All block
producers have been affected by a memory corruption that was caused by an
automatic resize of a `flat_index` container that resulted in an unrecoverable
stale state.

After several core developers debugging the code, the cause was identified and
a patch was quickly delivered to the block producers. Shortly after that, the
blockchain recovered and new blocks have been generated.

All transaction that made it into the blockchain prior to this incident have
been unaltered.

Unfortunately, the nature of the patch **requires all nodes to apply the
patch**, accordingly, in order to sync back with the blockchain. We recommend
exchanges and third party providers to update their backend to tag
`v2.0.170710` and rebuild. The following steps facilitate this update:

    git fetch
    git checkout v2.0.170710
    git submodule update --init --recursive
    make

### Acknowledgement

The BitShares Foundation would like to thank the core developers for their
short response time and for resolving the issue in a timely manner.

### Announcement Mailing List

In order to improve responsiveness, the BitShares Foundation has set up several
mailing lists including a low noise `announcements-critical` that we recommend
exchanges and partners of BitShares to [subscribe
to](http://lists.bitshares.foundation). This reduces the latency for exchanges
for receiving alert messages regarding the BitShares network.

### Technical Description and Patch Description

The incident caused the block production to halt due to bitasset data for
the `GAS` asset (`2.4.0`) returning an object id `0.0.0`. Since object ids
are supposed to not change, this has lead the BitShares developers to believe
that a memory corruption caused the assertion.

After several attempts to identify the cause of the memory corruption, Daniel
Larimer gave the crucial hint about the potential of a `flat_index` container
corrupting the memory on a resize.

A simple [two line
patch](https://github.com/bitshares/bitshares-core/commit/67804359693168f16db98b40319593b64b6a9eed)
replacing the `flat_index` container with a `generic_index` container solved
the memory corruption and thus the block production issue. Going forward, all
`flat_index` containers are going to be replaced by the more robust generic
implementation.
