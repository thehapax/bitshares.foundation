---
language: en
layout: worker
type: budget
bfid: 201903-atomic-cross-chain-swaps
workerid:
title: "JavaScript: Atomic Cross-Chain Swaps Framework"
name: Everbloom
company:
 name: Everbloom
 url: https://everbloom.co/
discussions:
# - name: bitsharestalk
#   url: 
# - name: steemit
#   url: 
price: $120,000 (in CNY)
duration: 20 weeks
start: 2019/03/01
end: 2018/09/30
paymentaccount:
---

# JavaScript: Atomic Cross-Chain Swaps Framework

## Background

With [BSIP44](https://github.com/bitshares/bsips/blob/master/bsip-0044.md), *Hash Timelocked Contracts* (HTLC) will become available on the BitShares Blockchain.
An HTLC is a conditional transfer where an encumbrance must be remedied to complete successfully. The BitShares Hashed Timelocked Contract implementation permits a designated party “recipient” to receive funds by disclosing the preimage of a hash (think: a password to claim a deposit) prior to an expiration timeout. It also permits the initiating party “depositor” to receive their deposited funds back if the  timeout is reached, in a refund situation.

This allows two parties to exchange tokens on independent platforms trustlessly and securely and thus enables Atomic Cross-Chain Swaps (ACCS) among other useful functionalities.

For ACCS, an HTLC is used in combination with the corresponding HTLC-like feature on the another blockchain. Many existing blockchain technologies support HTLC already, such as Ethereum ([example smart contract](https://www.npmjs.com/package/ethereum-htlc)), [Bitcoin](https://github.com/bitcoin/bips/blob/master/bip-0199.mediawiki), [Comodo](https://komodoplatform.com/atomic-swaps/), or [NEM](https://nemtech.github.io/concepts/cross-chain-swaps.html). A generalized application of HTLC is called Hash Time-Locked Agreements (HTLA) which is more commonly known as [Interledger](https://interledger.org/rfcs/0022-hashed-timelock-agreements/draft-1.html).

The implementation of HTLC in bitshares-core enables the functionality on the BitShares Blockchain. This worker proposal intends to develop a JavaScript framework on top of this feature to enable ACCS with Ethereum ERC-20 compatible tokens and allow easy integration into existing front-ends, such as the reference bitshares-ui, to expose the feature to a wider audience. The intention is to at least enable easy ACCS between the BitShares and Ethereum Blockchain.

We are convinced that the proposed framework for ACCS in this worker proposal can reshape the entire exchange landscape once it is easy to use for customers. Given that we operate Everbloom, an exchange based on top of Ethereum, we believe that we can gain a first mover advantage by enabling ACCS on our exchange. As we believe in the spirit of Open Source, and because we want a tight integration into bitshares-ui, we chose to engage the BitShares community to support the development of an open source library for ACCS. If this proposal is accepted by the community, we see a win-win scenario, where we increase our customer base and BitShares benefits from a tight integration into Everbloom.

## Requirements

Provided that ACCS is based on HTLCs which has been approved with BSIP44 and is currently in TESTNET for review by the community, we would like to point out that our work on the proposed framework highly depends on the successful deployment into MAINNET.

Since, BSIP44 is installed on the public testnet, we have a starting point for our implementation and integration with a local development-instance of the BitShares Blockchain. Ideally, we can provide a working demo prior to MAINNET deployment.

Furthermore, this framework highly depends on the HTLC implementation on other blockchains. Since we intend to integrate with Ethereum first, we may need to first audit existing smart contracts that implement HTLC which could lead to adaptation of our milestones and timelines.

This worker proposal intends to fund the development of an open source Javascript framework that implements ACCS based on HTLCs and, as such, is looking for funding of said feature to pay for development and consultancy hours.

## Deliverables

The goal of this worker proposal is to develop an open source framework for ACCS that is capable of integrating with multiple blockchains and initially provides adapters for ACCS operationsacross at least two blockchains (Bitshares and Ethereum). The framework should be architectured with usability **and** security in mind and the architecture is supposed to allow adding other blockchains to it with little effort.

The final delivery will constitute:

* **Javascript Framework**:
  The Javascript framework will integrate with the BitShares and the Ethereum Blockchain to allow ACCS. The goals of this library is to simplify and mostly automate ACCS for the customer and allow easy integration into existing applications and libraries. It will create and broadcast initial ACCS setup, monitor the blockchains for intermediary steps and finalize the swaps accordingly.
* **Unit & integration tests**:
  Unit tests are used to ensure that individual parts of the software behave as specified. Integration tests will ensure that these parts work together properly.
* **Specifications and Documentation**:
  The specifications will give a concise picture about the system architecture while documentation will provide implementation details.
* **Demo Application to facilitate ACCS**:
  A separate demo application is implemented that connects corresponding **testnets** and allows ACCS across them. The purpose of the demo, on the one hand, is that it shows to the end-user how it works while not risking any funds. On the other hand, it presents integration details to developers that seek to integrate the library with their own platform.

The library is supposed to be implemented such that it allows integrating HTLCs of additional blockchains easily.

### Demo Application Workflow

In the Demo Application, Alice and Bob want to swap two assets on different blockchains. Alice has BTS, Bob as ETH, but they both want what the other has.

A successful process looks as follows:

1. Setup Phase: before creating any HTLCs, Alice and Bob needs to first agree on parameters.
   1. How many BTS and ETH they intend to swap; their exchange rate.
   2. How long should the time-lock on the HTLC be active?
   3. Alice's receiving account on Ethereum.
   4. Bob's receiving account on BitShares.
   5. Who will generate the secret (the "Pre-Image") and the hash of the secret (the "Hash"). For the sake of this example, Alice will chose the Pre-Image and Hash creator.
2. Creation Phase: having agreed on the parameters, Alice and Bob create the HTLCs.
   1. Alice creates an HTLC on Bitshares with the receiver as Bob. BTS is locked into the BitShares HTLC. She shares the location of the BitShares HTLC with Bob. By doing so, she implicitly shares the Hash with Bob.
   2. Bob waits for the HTLC to confirm on the BitShares blockchain and validates all parameters, including but not limited to, that he is the receiver, that the amount is appropriate, and the HTLC hash-lock matches the agreed upon Hash.
   3. Bob creates an HTLC on Ethereum with the receiver as Alice. ETH is locked in the Ethereum HTLC.
   4. Alice waits for the HTLC to confirm on the Ethereum blockchain and validates that she is the receiver and the HTLC hash-lock matches the agreed upon Hash.
3. Redemption Phase: with the HTLCs created on both blockchains, Alice and Bob can now proceed to redeeming their new coins.
   1. Alice redeems the ETH on Ethereum by redeeming the HTLC by submitting the Pre-Image in a transaction. In doing so, she exposes the Pre-Image.
   2. Bob waits for Alice to expose the Pre-Image, and then Bob redeems the HTLC on BitShares using the same Pre-Image.
4. Everyone is now done.

## Milestones

These milestones serve as information to the BTS voters that evaluate this worker proposal. The milestones are used by the escrow to judge proper delivery.

The milestones are given in order of completion with an estimated hours of work involved for each milestone. 

1. Create Wireframes for Demo Application (10%, 160 hours)
   1. Wireframes should illustrate the Demo Application Workflow as described in a section above.
2. Architect the Demo Application (10%, 160 hours)
   1. Define the structure of the Demo Application beyond the UI.
   2. The architecture should provide for communication across clients to facilitate the sharing of ACCS information necessary to perform a complete swap.
3. Implement Demo Application MVP on Testnet (40%, 640 hours)
   1. Given the Wireframes and Architecture, implement a complete Demo Application.
4. Extract Framework from Demo Application (25%, 400 hours)
   1. Implement Framework in Javascript
   2. Integration for the BitShares Blockchain
   3. Integration for the Ethereum Blockchain
   4. Unit Tests
Proper documentation of the entire flow and the interface (15%, 240 hours)

## Requesting Funding / Budget

The total estimated hours of effort is 1600 hours. Everbloom intends to put two developers working 40 hours per week onto the project. This results in a five month completion time as shown in the following math:

1600 hours / 2 devs / 40 hours per week / four weeks per month = 5 months## Requesting Funding / Budget

2 full-time software engineers ($75/hr)
2 developers * 40 hours * $75 per hour * (up to) 20 weeks = (up to) **$120,000**

## About Everbloom
Everbloom is a venture-backed, decentralized cryptocurrency exchange that has raised $2M in capital to build an enterprise grade trading marketplace for institutional investors. The company is founded by successful serial entrepreneurs with prior startups that achieved revenue in excess of $30M annually and raised over $70M in capital. Today, The Everbloom Exchange supports the trading of digital assets built on top of the Ethereum blockchain. The company is headquartered in Boston, MA, USA. Everbloom was [recently covered by CoinDesk](https://www.coindesk.com/why-a-decentralized-crypto-exchange-is-seeking-a-securities-license/), one of the largest blockchain publications.

### Links

* Website: everbloom.co
* Exchange: app.everbloom.co
* User docs: docs.everbloom.co
* API docs: docs.api.everbloom.co
* Twitter: twitter.com/EverbloomHQ
* Blog: medium.com/Everbloom
* Telegram Chat: t.me/EverbloomHQ

### Everbloom Team

For more information about the Everbloom team, please see [About Everbloom](https://everbloom.co/about/).
