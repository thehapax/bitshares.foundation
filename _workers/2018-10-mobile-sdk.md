---
language: en
layout: worker
type: budget
bfid: 201810-mobile-sdk
workerid:
title: OpenSource BitShares Mobile SDK (android/ios)
name: Blockchain BV
company:
 name: Blockchain BV
 url: http://blockchainprojectsbv.com
discussions:
 - name: bitsharestalk
   url:
 - name: steemit
   url:
price: up to 75,000 €/bitEUR
duration: 
start: 2018/10/01
end: 2018/12/31
paymentaccount: blockchain-bv
---

# Intent

Over the last months, we at Blockchain Projects have seen a lot of
demand for mobile applications running on top of BitShares and allowing
to use tokens.

The desire to have a mobile application capable of transacting with
BitShares has motivated us to start development long ago. 

What is not widely known is that we have a mobile application framework
for BitShares that allows to develop and customized a variety of mobile
apps for the BitShares Blockchain. Among this, we have developed what is
needed to provide UIA support for loyalty (or similar) program with
sponsoring and promotion screens and listings and a KYC registration
framework.

This framework, or Software Development Kit (SDK) is highly
customizable, allows for company-specific branding and is built entire
using React-native/redux - a widely known framework that supports
Android as well as iOS.

The intention of this worker proposal is to cover the costs of our
development and receive funding to continue our work on the SDK.

# State of the Art

Our BitShares mobile framework comes with the following functionalities:

* **Multiasset** support
* **Multiaccount** support and account management
* **Wallet** creation/backup/import
* Key import and **encrypted storage** (pin)
* Account **registration** via standard faucets
* **Memo** support
* **Mainnet** and **Testnet** support
* Account **history**
* **QR code** scanner, payment format and **QRLogin**
* **Request Money** Screen
* I18n and **language support**
* Custom **sponsoring** screens and listings
* Easy customization through **branding**

**[Screenshots](2018-10-mobile-sdk/)**

# Deliverables

This worker delivers, in case it is accepted by the community, the
sources of a fully functional mobile wallet development toolkit
that builds to a mobile wallet app today.

The community will be free to leverage this software delivery to build
their own products based on this framework, such as the usual UIA
use-cases: Remittance, Loyalty programs, service coins, prepaid cards
etc.

Our delivery focuses on:
* code base as git repository
* unit testing
* basic UI/UX
* build toolchain for Android and iOS
* continuous integration (e.g. into gitlab)
* technical documentation

# Milestones/Delivery and Costs

Provided that the code is at a stable state today, we propose the
following:

* **On Approval** - BitShares-UI^1 team is granted access to the
  (closed-source and proprietary) repository after signing a
  Non-Disclosure Agreement with us.
* **After €50k** - The code is published under proprietary license. We
  start implementing according to feedback provided by BitShares-UI
  team.
* **After €75k** - SDK is open-sourced under GPL.
* Support and consultation for the provided code is provided until end
  of Q4/2018.

# Fineprint

* This worker pays in **bitEUR/€** instead of bitUSD/$
* The Terms & Conditions of Blockchain Projects BV apply with the BitShares DAC being referred to as Client
* Blockchain Projects BV to perform and assist with delivery and coordination
* ^1: The "BitShares-UI team" being the team working on the `bitshares-ui` repository in the github `bitshares` organization.
