---
title: Asset Creation Temporarily suspended
layout: announcement
---

On Wednesday, October 18th 2017, an
[issue](https://github.com/bitshares/bitshares-core/issues/429) was
reported by [@abitmore](https://github.com/abitmore), one of our core
developers about an inaccuracy due to rounding when creating a new asset
on the BitShares platform.

Shortly after, he approached other core developers about further
findings that need immediate attention. The core of the problem lies in
[this line](https://github.com/bitshares/bitshares-core/blob/2.0.170710/libraries/chain/asset_evaluator.cpp#L94),
[this line](https://github.com/bitshares/bitshares-core/blob/2.0.170710/libraries/chain/asset_evaluator.cpp#L127),
and
[this line](https://github.com/bitshares/bitshares-core/blob/2.0.170710/libraries/chain/evaluator.cpp#L89),
and would have allowed an user to obtain free BTS tokens by crafting an
`asset_create_operation` in a certain way. [Full
Disclosure](https://github.com/bitshares/bitshares-core/issues/433).

After confirming the issue on the [public
testnet](https://testnet.bitshares.eu), the developers approached the
committee and requested to **disable asset creation** until a fix has
been deployed to the network. The proposal has been approved quickly
which renders asset creations **temporary disabled**.

That said, the *bug* cannot be exploited any longer and a fix is
currently tested.

## Effects on End-Users

End-users that wanted to create an asset on BitShares are asked for
patience until the fix has been deployed. No other restrictions are
expected.

## How will this be fixed

The core developers are currently in discussion on the best way forward.
The options are to wait for the newly scheduled hard fork later this
year, or deploy an additional soft-fork to be able to re-activate asset
creation and continue full service.

## Remark

In contrast to rumours, the suspension of Asset creation has nothing to
do with compliance or other legal aspects of the platform and merely
prevents a bug from being exploited.
