---
title: Asset Creation Reactivated
layout: announcement
---

Thanks to back-end developers of BitShares, a new
[release](https://github.com/bitshares/bitshares-core/releases/tag/2.0.171019a)
has been tagged that fixes the [bug that was discovered
yesterday](https://github.com/bitshares/bitshares-core/issues/433) and
that led to the committee disabling asset creation, temporarily.

It is our pleasure to announce that the BitShares blockchain is fully
operational again, including asset creation at the expected fees.

We, the BitShares Blockchain Foundation would like to thank the back-end
developers that solved the issue so quickly as well as the committee
members that assisted in making sure the bug cannot be exploited.
Furthermore, we would like to thank the block producers (witnesses) for
deploying the fix so quickly and allowing to go back into normal
operation mode, today.

We would like to remark, that due to the technical superiority of
BitShares and its governance process, a network upgrade (as *soft fork*)
was deployed in **less than 24 hours**.

## Affected Users

The upgrade was deployed so quickly as it was implemented as a
*soft-fork*. This patch ensures that the bug cannot be exploited by
requiring the fee for `asset_creation_operation` to be paid in `BTS`.
This restricts users slightly as they cannot pay the fee in any other
asset than `BTS`. We apologize for this inconvenience, and plan to
include a proper update in the upcoming hard-fork that is planned for
November (more about this to be released soon).

## Who has to update:

* Witnesses are **REQUIRED** to upgrade to this release as soon as possible.
* Seed nodes are **RECOMMENDED** to upgrade.
* other nodes may upgrade **OPTIONALLY**
