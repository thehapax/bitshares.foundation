---
title: BitShares Backend Crash Incident after Malformed Proposal
layout: announcement
---

On Monday, December 20th 2018 at block height 33,269,102, an incident occurred on the BitShares network that caused some backend nodes to crash with errors such as

* `counter < db.get_global_properties().active_witnesses.size() * 2: Max proposal nesting depth exceeded!`
* `Proposed transaction 1.10.17503 failed to apply once approved with exception:`
* `Internal error: static_variant tag is invalid.`

Upon restart, most backend machines restarted and replayed to the current state of the blockchain just fine. However, a few backend nodes have been stuck with an inconsistent state caused by a proposal.

### Root cause
A special crafted proposal made it onto the blockchain which caused a chaining of events that lead to memory corruption and crashes on some machines.

### Impact
This incident had some impact on API and backend nodes and caused crashes. Most backend nodes could automatically recover from the crash and continue to operate.

During a period of about 30 minutes, roughly 40% of the block producers had stopped producing blocks which lead to a participation rate of less than 60%. As a consequence, the last irreversible block (LIB) did not advance for said period. After crashed block producers had been voted out, participation rate increased significantly and the LIB continued to advance. At this point, we would like to emphasise that 3rd parties and exchanges should ensure they operate on the LIB (by means of the delayed node) as recommended in documentation.

We would like to reassure that:
* No funds have been at a risk
* There were no forks

### Solution
The Core Team has created a new release of the BitShares core software that works around the problem and will prevent similar issues in the future. All nodes are **required to upgrade** to the latest release tag, named:

    2.0.181221

We recommend exchanges and third party providers to update their back-end to tag `2.0.181221` and rebuild. The following steps facilitate this update:

    git fetch
    git checkout 2.0.181221
    git submodule update --init --recursive
    make

If you are using the official docker container, please allow some time for the container to be built by the docker cloud.

The BitShares Core Team reacted promptly and professionally to identify the root cause and issue an emergency patch. A [Release](https://github.com/bitshares/bitshares-core/releases) was posted on GitHub for all nodes to upgrade their running software. [This Patch](https://github.com/bitshares/bitshares-core/pull/1484/files) fixes the issue and prevents it from reappearing in the future.

### Acknowledgement
The BitShares Blockchain Foundation would like to thank the core developers for their short response time and for resolving the issue in a timely manner.

### Announcement Mailing List
In order to improve responsiveness, the BitShares Blockchain Foundation has set up several mailing lists including a low noise `critical` and an `announcement` list that we recommend fundamental industry partners (like exchanges and money transmitting partners) to [subscribe to](http://lists.bitshares.foundation).
This will enable all businesses in the BitShares network to be aware of all latest developments.
