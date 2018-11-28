---
title: BitShares Block Production Incident Report
layout: announcement
---

On Monday, November 27th 2018 at block height 32,599,932, an incident occurred
on the BitShares network that caused an unplanned interruption of block
production. All nodes have been affected by an overflow issue in the protocol
that deals with collateral bidding after global settlement.

After gathering of the core developers and debugging the code, the cause was
identified quickly and a patch was immediately delivered to the block
producers. Shortly after that, the blockchain recovered and new blocks have
been generated.

It is absolutely necessary that everyone is aware that the nature of the patch
**requires all nodes to apply the patch**, accordingly, in order to sync back
with the blockchain. We recommend exchanges and third party providers to update
their back-end to tag `2.0.181127` and rebuild. The following steps facilitate
this update:

    git fetch
    git checkout 2.0.181127
    git submodule update --init --recursive
    make

If you are using the official docker container, please allow some
time for the container to be built by the docker cloud.

We would like to reassure that:
* No fund have been at a risk
* There were no forks

### Acknowledgement

The BitShares Blockchain Foundation would like to thank the core developers for
their short response time and for resolving the issue in a timely manner.

### Announcement Mailing List

In order to improve responsiveness, the BitShares Blockchain Foundation has set
up several mailing lists including a low noise `critical` and an `announcement`
list that we recommend fundamental industry partners (like exchanges and money
transmitting partners) to [subscribe to](http://lists.bitshares.foundation).
This will enable all businesses in the BitShares network to be aware of all
latest developments.

## Root Cause

Collateral bids for settled assets are only processed during maintenance. At
least one bid was out of bounds and caused the processing overflow.

Prior to the halt, validation software did not contain code to properly check
for an overflow condition within the method used to bid collateral for debt in
the global settlement pool of an asset. In this case, the asset bitUSD was in
the global settlement state, and a bidder submitted a transaction containing a
bid operation that exceeded the total supply of available bitUSD within the
settlement pool. During the maintenance period, at least one overflow condition
was caught by the software which prevented the bid operation from being
included as a valid transaction. However, this did not fail gracefully and
caused the block producing nodes to halt.

##Resolution

The BitShares Core Team reacted promptly and professionally to identify the
root cause and issue an emergency patch. Once the patch was validated and
issued to Block Producers to restart the network, a
[Release](https://github.com/bitshares/bitshares-core/releases) was posted on
GitHub for all nodes to upgrade their running software.

[The patch](https://github.com/bitshares/bitshares-core/commit/5b2309931c441412234c3bd09f39b41969c74dcc)
fixes this by treating the amount provided in the price correctly and prevent
an overflow.
