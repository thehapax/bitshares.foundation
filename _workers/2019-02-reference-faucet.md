---
language: en
layout: worker
type: escrow
bfid: 201902-reference-faucet
workerid:
title: Maintaining the Reference faucet
name: BitShares Europe
company:
 name: ChainSquad GmbH
 url: http://chainsquad.com
discussions:
 - name: bitsharestalk
   url: 
 - name: steemit
   url: 
price: 3360 bitEUR (280€/mth)
duration: 12 months
start: 2018/02/01
end: 2019/01/31
paymentaccount: chainsquad
---

## BitShares Reference Faucet

The community-funded reference faucet has already been operated
through [BitShares Europe](https://bitshares.eu) as a subcontractor to
Blockchain Projects B.V. who has been granted the right to operate the
reference faucet as part of their
[infrastructure](https://www.bitshares.foundation/workers/2018-07-infrastructure)
program.

BitShares Europe (operated through ChainSquad GmbH) here proposes to
continue operating and maintaining the reference faucet **identically** to
the previous worker proposal:

* default faucet used by the reference web/light client implementation
* registrar account is owned by the BitShares community (through committee account and the BBF)
* referral rewards to fund account create only
* no default proxy
* excessive funds to be returned to the working budget of the BitShares Blockchain

Thus, the **registrar** account `onboarding.bitshares.foundation`
remains and is owned by the committee-account. The BitShares Blockchain
Foundation has agreed to allow ChainSquad GmbH to operate the
`onboarding.bitshares.foundation` account on trust. The referral
percentage for affiliates remains at **70%**. This means that

* 30% of the referral rewards go to the onboarding account
* 70% of the reward go to the referrer, if no referrer is present, the
  registrar (onboarding account) will be used.

As of January 10th, BitShares Europe has registered **over 100,000
accounts** for the BitShares Community. Of those, almost **500 accounts
upgraded** to life-time member. Greater details are provided
[online](https://bitshares.eu/referral/onboarding/onboarding.bitshares.foundation).

## Deliverables & Conditions

BitShares Europe will provide a reliable (3x redundant) infrastructure
that operates the reference faucet at:

    https://faucet.bitshares.eu/onboarding

The faucet operates behind SSL and a loadbalancer that comes with 3x
redundancy. The Onboarding registrar allows for custom referrers to be
provided with the `r=?` parameter to reference wallet deployments (such
as `wallet.bitshares.org`).

## Price

Operating faucets is a Business2Business services provided through
BitShares Europe, a product of ChainSquad GmbH. That service has a price
tag of 400€ per month.

The BitShares community receives a **30% discount** which results in
280€/month (~$300/mth).

The worker proposals desires to fund operations for a duration of a full
year.

## Remarks

* We would like to remind everyone about time and IP-based restrictions
  that are put in place to prevent abuse of this community services.
  Commercial use of this faucet is discouraged.
