---
title: BitShares Core Release 2.0.180425
layout: announcement
---

The BitShares Blockchain Foundation is pleased to let everyone know about the *upcoming* protocol upgrade for the BitShares main network.

After months of development and many weeks of testing on the [bitshares testnet](https://testnet.bitshares.eu), the finalized version

    2.0.180612

has been tagged in [bitshares-core](https://github.com/bitshares/bitshares-core).

**Important remark:**
This is a *protocol upgrade release*. **All** nodes must upgrade before `2018-07-19 14:00:00 UTC`.

* If you're upgrading from `2.0.180425` to `2.0.180612`, you don't need to do anything special;
* if you're upgrading from a release earlier than `2.0.180425` to `2.0.180612`, please check [release notes of 2.0.180425](https://github.com/bitshares/bitshares-core/releases/tag/2.0.180425) to see if you need to perform additional steps.

## Major Updates

* [BSIP26: Refund Order Creation Fee in Originally Paid Asset when order is cancelled](https://github.com/bitshares/bsips/blob/master/bsip-0026.md)
* [BSIP27: Asset Issuer Reclaim Fee Pool Funds](https://github.com/bitshares/bsips/blob/master/bsip-0027.md)
* [BSIP29: Require owner authority to change asset issuer](https://github.com/bitshares/bsips/blob/master/bsip-0029.md)
* [BSIP30: Always Allow Increasing Collateral Ratio If Debt Not Increased](https://github.com/bitshares/bsips/blob/master/bsip-0030.md)
* [BSIP31: Update Short Position's Margin Call Price After Partially Called Or Settled](https://github.com/bitshares/bsips/blob/master/bsip-0031.md)
* [BSIP32: Always Match Orders At Maker Price](https://github.com/bitshares/bsips/blob/master/bsip-0032.md)
* [BSIP33: Maker Orders With Better Prices Take Precedence](https://github.com/bitshares/bsips/blob/master/bsip-0033.md)
* [BSIP34: Always Trigger Margin Call When Call Price Above Or At Price Feed](https://github.com/bitshares/bsips/blob/master/bsip-0034.md)
* [BSIP35: Mitigate Rounding Issue On Order Matching](https://github.com/bitshares/bsips/blob/master/bsip-0035.md)
* [BSIP36: Remove expired price feeds on maintenance interval](https://github.com/bitshares/bsips/blob/master/bsip-0036.md)
* [BSIP37: Allow new asset name to end with a number](https://github.com/bitshares/bsips/blob/master/bsip-0037.md)
* [BSIP38: Add target collateral ratio option to short positions](https://github.com/bitshares/bsips/blob/master/bsip-0038.md)
* [Bugfix #184: Potential something-for-nothing fill bug](https://github.com/bitshares/bitshares-core/issues/184)
* [Bugfix #214: Proposal cannot contain proposal_update_operation](https://github.com/bitshares/bitshares-core/issues/214)
* [Bugfix #453: Multiple limit order and call order matching issue](https://github.com/bitshares/bitshares-core/issues/453)
* [Bugfix #588: Virtual operations should be excluded from transactions](https://github.com/bitshares/bitshares-core/issues/588)
* [Bugfix #868: Clear price feed data after updated a bitAsset's backing asset ID](https://github.com/bitshares/bitshares-core/issues/868)
* [Bugfix #890: Update median feeds after feed_lifetime_sec changed](https://github.com/bitshares/bitshares-core/issues/890)
* [Bugfix #922 / #931 / #970] Fixed missing checks when updating a smart coin's `bitasset` options E.G. force settlement delay, backing asset ID or etc;
* [Bugfix #942] Fixed missing asset authorities check for "from" account when claiming from a withdraw permission.

[**Complete Release Notes**](https://github.com/bitshares/bitshares-core/releases/tag/2.0.180612)

## How to upgrade from sources

    git fetch origin
    git checkout 2.0.180612
    git submodule sync --recursive
    git submodule update --init --recursive

    # it follows the usual compile instructions with cmake and make

## Change Log

The detailed lists about bug and security fixes can be found in the [Release
Notes](https://github.com/bitshares/bitshares-core/releases/tag/2.0.180425)

## Docker

The new docker container has been built by Docker Hub and is available via

    docker pull bitshares/bitshares-core:2.0.180612
