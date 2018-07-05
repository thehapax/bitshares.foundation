---
title: BitShares Block Production Incident Report
layout: announcement
---

TEst

On Monday, July 10th 2017 at 9:00am UTC, an incident occurred on the BitShares
network that caused an unplanned interruption of block production. All block
producers have been affected by a memory corruption that was caused by an
automatic resize of a `flat_index` container that resulted in an unrecoverable
stale state. This has happened for the first time in over two years of
blockchain operations.

After several core developers debugging the code, the cause was identified and
a patch was quickly delivered to the block producers. Shortly after that, the
blockchain recovered and new blocks have been generated.

All transaction that made it into the blockchain prior to this incident are
unaltered!

It is absolutely necessary that everyone is aware that the nature of the patch
**requires all nodes to apply the patch**, accordingly, in order to sync back
with the blockchain. We recommend exchanges and third party providers to update
their back-end to tag `2.0.170710` and rebuild. The following steps facilitate
this update:

    git fetch
    git checkout 2.0.170710
    git submodule update --init --recursive
    make

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

### Technical Description and Patch Description

The incident caused the block production to halt due to bitasset data for
the `GAS` asset (`2.4.0`) returning an object id `0.0.0`. This error was
triggered during a maintenance interval and threw an assertion that prevented
block producers from producing blocks. Since object ids are supposed to not
change, this has lead the BitShares developers to believe that a memory
corruption caused the assertion.

While attempting to identify the cause of the memory corruption, Daniel
Larimer gave the crucial hint about the potential of a `flat_index`
container corrupting the memory on a resize.

A simple [five line patch](https://github.com/bitshares/bitshares-core/commit/67804359693168f16db98b40319593b64b6a9eed)
replacing the `flat_index` container with a `generic_index` container solved
the memory corruption and thus the block production issue. Going forward, all
use of `flat_index` is revisited and a general replacement by `generic_index`
will be [evaluated and tested](https://github.com/bitshares/bitshares-core/issues/325).

#### Update - Wed Jul 12

As it turned out after further investigation, the root cause was an
inappropriate implementation of [`flat_index::remove`](https://github.com/bitshares/bitshares-core/blob/master/libraries/db/include/graphene/db/flat_index.hpp#L73)
that only zeroed an entry instead of removing the whole element from the
container. What happens is that a new bitasset has been proposed but the
proposal wasn't fully approved. The bitasset data was created in the
database and then zeroed instead of being removed after expiration of
the proposal. This is the first time in the history of our chain when
`flat_index::remove` was called.

The conclusion is that `flat_index` is not made for having items
removed. Proposals can always lead to items being removed, which means
that `flat_index` is not suitable for the job and should be replaced in
all places.
