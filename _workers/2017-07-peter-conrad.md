---
title: Implementation of BSIP-18
name: Peter Conrad
company:
 name: Cyrano UG (haftungsbeschränkt)
 url: http://bts.quisquis.de/impressum.html
layout: worker
status:
  proposal-vetted: True
  worker-created: False
  worker-approved: False
  worker-paying: False
  worker-finished: False
payments:
reports:
price: $23k
duration: 2 months
---

# Worker Proposal

This document presents a worker proposal to the BitShares shareholders curated and 
supported by the BitShares Foundation. We see a need for a few updates on the BitShares
network and would like begin with the proposed work below. Further more, we are happy
to announce that we already have a freelancer that is taking up this task for us:

**Peter Conrad**, also known as @pc and a knowledgable and long-standing member of the
community and active developer for years.

# Proposed Work

I propose to implement the functionality described in the
[BSIP-0018](https://github.com/bitshares/bsips/blob/master/bsip-0018.md)
consisting of

* fixing the bug preventing settlement after a black swan
* re-allowing price feeds after a black swan
* the automatic revival of MPAs when the value of the settlement fund
  exceeds the nominal value of the total supply by more than the MCR
* the bidding of additional collateral for a part of the debt and the
  associated part of the settlement fund
* the revival of MPAs after sufficient bids have been made

## Milestones

My work includes the following milestones:

* 20% specification (already delivered, see BSIP-0018)
* 30% implementation (mostly finished)
* 10% integration into testnet (*)
* 10% testing (*)
* 10% bugfixes
* 10% integration into mainnet, including release (*)
*  5% supervision of hardfork (*)
*  5% supervision of initial coordinated MPA revival after hardfork (*)

I expect the current witnesses to actively assist in the items marked with (*).
It is their responsibility to maintain the operation of the chain, and
ultimately it is their decision which version of bitshares-core they use to
produce blocks. With the current price of BTS, witness pay should be sufficient
reward for their efforts.

The milestones are verified and validated by ChainSquad GmbH on behalf of
BitShares Foundation.

This means that the shareholders obtain a ready-to-run and tested patch that to
be included in the BitShares network through a hardfork.

# Payment

The package is priced at 23k bitUSD. This fee includes

 * all expenses for production,
 * testing,
 * account and worker setup fee,
 * escrow setup and maintenance,
 * worker bitUSD-payment management,
 * code quality assurance,

and is asked to be paid through a BitShares worker.

The freelancer applies additional rules:

* I accept a fixed amount of bitUSD as payment. That means I do not profit from
  a BTS price increase. It also means that I will not suffer a loss from a BTS
  price drop. If the BTS price drops and as a result the worker payment is not
  sufficient to pay me out, an additional worker will have to be set up to make
  up for this.

* If the shareholders decide to vote the worker out before it covers the
  payment I'm asking, I will stop working on the project. I will receive the
  full amount paid to the worker up to that point, in proportion to the work
  I have already delivered (see milestones above).

* My full work will be delivered under the terms of the MIT license. In
  particular, the disclaimer applies.
