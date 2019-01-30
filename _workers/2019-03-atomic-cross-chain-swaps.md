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
price: $96,000 (in CNY)
duration: 6 months
start: 2019/03/01
end: 2018/09/30
paymentaccount:
---

# JavaScript: Atomic Cross-Chain Swaps Framework

## Background

With [BSIP44](https://github.com/bitshares/bsips/blob/master/bsip-0044.md), *Hashed Time-Locked Contracts* (HTLC) will become available on the BitShares Blockchain.
An HTLC is a conditional transfer where an encumbrance must be remedied to complete successfully. The BitShares Hashed Time-Locked Contract implementation permits a designated party “recipient” to receive funds by disclosing the preimage of a hash (think: a password to claim a deposit) prior to an expiration timeout. It also permits the initiating party “sender” to receive their deposited funds back if the timeout is reached, in a refund situation.

This allows two parties to exchange tokens on independent platforms trustlessly and securely and thus enables Atomic Cross-Chain Swaps (ACCS) among other useful functionalities.

For ACCS, an HTLC is used in combination with the corresponding HTLC-like feature on the other blockchain. Many existing blockchain technologies support HTLC already, such as Ethereum ([example smart contract](https://www.npmjs.com/package/ethereum-htlc)), [Bitcoin](https://github.com/bitcoin/bips/blob/master/bip-0199.mediawiki), [Comodo](https://komodoplatform.com/atomic-swaps/), or [NEM](https://nemtech.github.io/concepts/cross-chain-swaps.html). A generalized application of HTLC is called Hash Time-Locked Agreements (HTLA) which is more commonly known as [Interledger](https://interledger.org/rfcs/0022-hashed-timelock-agreements/draft-1.html).

The implementation of HTLC in bitshares-core enables the functionality on the BitShares Blockchain. This worker proposal intends to develop a JavaScript framework on top of this feature to enable ACCS with Ethereum ERC-20 compatible tokens and allow easy integration into existing front-ends (such as the reference bitshares-ui) to expose the feature to a wider audience. The intention is to at least enable easy ACCS between the BitShares and Ethereum Blockchain.

We are convinced that the proposed framework for ACCS in this worker proposal can reshape the entire exchange landscape once it is easy to use for customers. Given that we operate Everbloom, an exchange based on top of Ethereum, we believe that we can gain a first mover advantage by enabling ACCS on our exchange. As we believe in the spirit of Open Source, and because we want a tight integration into bitshares-ui, we chose to engage the BitShares community to support the development of an open source library for ACCS. If this proposal is accepted by the community, we see a win-win scenario, where we increase our customer base and BitShares benefits from a tight integration into Everbloom.

## Requirements

Provided that ACCS is based on HTLCs which has been approved with BSIP44 and is currently in TESTNET for review by the community, we would like to point out that our work on the proposed framework highly depends on the successful deployment into MAINNET.

Since BSIP44 is installed on the public testnet, we have a starting point for our implementation and integration with a local development-instance of the BitShares Blockchain. Ideally, we can provide a working demo prior to MAINNET deployment.

Furthermore, this framework highly depends on the HTLC implementation on other blockchains. Since we intend to integrate with Ethereum first, we may need to first audit existing smart contracts that implement HTLC which could lead to adaptation of our milestones and timelines.

This worker proposal intends to fund the development of an open source Javascript framework that implements ACCS based on HTLCs and, as such, is looking for funding of said feature to pay for development and consultancy hours.

## Deliverables

The goal of this worker proposal is to develop an open source framework for ACCS that is capable of integrating with multiple blockchains and initially provides adapters for ACCS operations across at least two blockchains (Bitshares and Ethereum). The framework should be architectured with usability **and** security in mind and the architecture is supposed to allow adding other blockchains to it with little effort.

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

In the Demo Application, Alice and Bob want to swap two assets on different blockchains. Alice has BTS, Bob has ETH, but they both want what the other has.

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

These milestones serve as information to the BTS voters that evaluate this worker proposal. The milestones are used by the escrow to judge proper delivery. Any and all development will be done in public repositories.

1. Create Wireframes for Demo Application (10%)
2. Architect the Demo Application (10%)
3. Implement Demo Application MVP on Testnet (40%)
4. Extract Framework from Demo Application (25%)
   1. Implement Framework in Javascript
   2. Integration for the BitShares Blockchain
   3. Integration for the Ethereum Blockchain
   4. Unit Tests
5. Proper documentation of the entire flow and the interface (15%)

## Requesting Funding / Budget

* 2 full-time software engineers ($75/hr)

2 developers * 40 hours * $75 per hour * 16 weeks = **$96,000**

## About Everbloom
Everbloom is a venture-backed, decentralized cryptocurrency exchange that has raised $2M in capital to build an enterprise grade trading marketplace for institutional investors. The company is founded by successful serial entrepreneurs with prior startups that achieved revenue in excess of $30M annually and raised over $70M in capital. Today, The Everbloom Exchange supports the trading of digital assets built on top of the Ethereum blockchain. The company is in the process of obtaining a broker-dealer license from FINRA and recently announced a partnership with Makor Capital, an international multi-strategy hedge fund to provide additional liquidity and depth to its order book. The company is headquartered in Boston, MA, USA. Everbloom was [recently covered by CoinDesk](https://www.coindesk.com/why-a-decentralized-crypto-exchange-is-seeking-a-securities-license/), one of the largest blockchain publications.

### Everbloom Team

**Andrew Rollins**, *CEO (https://www.linkedin.com/in/andrewrollins/)*:

Bio: Andrew Rollins is the co-founder and former Chief Software Architect of Localytics, a Boston-based analytics firm founded in 2008. During his eight year tenure, Localytics achieved annual revenues of more than $25M, raised $60M in venture financing, measured over 2 billion mobile devices, processed over 5 billion datapoints per day, handled peaks of 100K+ transactions per second, and securely managed petabytes of data. As Chief Software Architect, he built a team of over 70 engineers and was directly responsible for petabyte scale cloud infrastructure. Andrew is also a former Microsoft software engineer and spent two years as a Venture Partner at Sigma Prime Ventures making Series A investments.
 
Everbloom role: Andrew is Everbloom’s CEO. He sets the company’s vision, product, and roadmap. Andrew works closely with the companies engineering team and leverages his deep technical toolkit when key engineering decisions need to be made.

**Scott Pirrello**, *COO (https://www.linkedin.com/in/scottpirrello/)*:

Bio: Scott Pirrello is the founder and former CEO of CampusSIMs ($6 million in VC financing, 20 employees), a well-known Boston based telecommunications and mobile company. During Scott’s six-year tenure as CEO, the company achieved a $6M annual revenue run-rate, had more than 10K active monthly paying subscribers and over 400 college and university partnerships including Harvard, MIT, NYU, and UCLA. The proprietary native mobile applications developed by the company are widely regarded as the top telecommunications activation apps in the United States.
 
Everbloom role: Role: As COO, Scott uses his past experience as an operator and innovator to set strategy,particularly in areas concerning business and product development, capital raising, and hiring. He handles logistics with partners and vendors. Scott led partnership formations with Makor Capital, Wyre, 0x, and Coindesk. Scott is a member of the company’s Board of Directors.

**Luke Chen**, *Senior Software Engineer*:

Bio: Luke Chen is part of the core engineering team at Everbloom. He is a full-stack senior software engineer that has deep experience building both enterprise and consumer grade software. In his career, he has built software for early stage emerging tech companies and mature companies with yearly revenue in excess of $100M. He is particularly proficient in back-end software development, Node.js, blockchain technologies, solidity, cloud computing, and more. He is bi-lingual, speaking both English and Mandarin. Luke received a Master’s of Science in Computer Science from George Washington University.
 
Everbloom role: Luke is responsible for system architecture, Ethereum nodes, databases, RESTful APIs, report generation, caching, and smart contract development at Everbloom. Over the past several months Luke has integrated FIAT pricing, token info, and Etherdelta/ForkDelta APIs, while also writing smart contracts which support compliant trading (KYC and AML), cross-protocol trading (Everbloom, 0x, EtherDelta), batch trading, market orders, limit orders, order matching, fee sharing, etc.

**Tongbo Sui**, *Senior Software Engineer (https://www.linkedin.com/in/tongbosui/)*:

Tongbo Sui is part of the core engineering team at Everbloom. He is a full-stack senior software engineer that has deep experience building both enterprise and consumer grade software. In his career, he has built software for early stage emerging tech companies and mature companies with yearly revenue in excess of $100M. He is particularly proficient in building well-structured, highly maintainable and extensible browser-side applications with JavaScript and other related tools. He also produces high quality software regarding cloud, blockchain and server-side applications. He is bi-lingual, speaking both English and Mandarin. Tongbo received a Master’s of Science in Computer Science from the University of Pennsylvania.
 
Everbloom role: Tongbo is responsible for developing Everbloom’s web app with client-side security features and high data update throughput. He has developed the complete set of UI/UX for the Everbloom web app and designed its architecture and build flow. Over the last several months he has built the event stream based web app with fully decoupled modularized rendering and data model logic, integration with RESTful APIs, Ethereum network information monitoring, and custom data structure that supports ordered state updates with high throughput and high frame rendering performance.

### Links

* Website: everbloom.co
* Exchange: app.everbloom.co
* User docs: docs.everbloom.co
* API docs: docs.api.everbloom.co
* Twitter: twitter.com/EverbloomHQ
* Blog: medium.com/Everbloom
* Telegram Chat: t.me/EverbloomHQ

## Summary to the Shareholder

This worker creates a easy-to-use framework for the integration of Atomic Cross-Chain Swaps (ACCS) 
(among other applications) which allows trustless and secure token swaps between independent platforms. This is an important step to facilitate the adoption of HTLC and a consequent extension of the BitShares Blockchain as a decentralized platform and its built-in DEX (decentralized exchange).

### BitShares contribution

This worker proposal provides funds for the software development of the framework and seeks to built a foundation for its adoption.

### Everbloom contribution

Everbloom will be the first to adopt the newly created framework on their exchange on the Ethereum blockchain and seek integration into the BitShares UI to enable interaction of both platforms. The necessary funds with respect to marketing and any promotional campaigns are not included in this proposal and are provided as the contribution of Everbloom.
