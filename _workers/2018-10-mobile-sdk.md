---
language: en
layout: worker
type: budget
bfid: 201810-mobile-sdk
workerid:
title: BitShares mobile SDK (android/ios)
name: Blockchain Projects BV
company:
 name: Blockchain Projects BV
 url: http://blockchainprojectsbv.com
discussions:
 - name: bitsharestalk
   url:
 - name: steemit
   url:
price: up to 75,000 €
duration: 
start: 2018/10/01
end: 2018/12/31
paymentaccount: blockchainprojects
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

* Wallet creation/backup/import
* Key import and encrypted storage (pin)
* Account Registration via standard faucets
* Multi-account support and account management
* Memo support
* Mainnet and Testnet support
* Account history
* QR code scanner, payment format and QRLogin
* Request Money Screen
* I18n and language support
* Custom sponsoring screens and listings

**[Screenshots](2018-10-mobile-sdk/)**

# Milestones/Delivery and Costs

Provided that the code is at a stable state today, we propose the
following:

* **On Approval** - BitShares-UI^1 team is granted access to the
  (closed-source and proprietary) repository after signing a
  Non-Disclosure Agreement with us.
* **After €50k** - The code is published and open-sourced under GPL. We
  start implementing according to feedback provided by BitShares-UI
  team.
* **After €75k** - MIT-license is granted.
* Support and consultation for the provided code is provided until end
  of Q4/2018.

# Remark

* Terms & Conditions of Blockchain Projects BV apply with the BitShares DAC being referred to as Client
* This worker pays in bitEUR/€ instead of bitUSD/$
* ^1: The "BitShares-UI team" being the team working on the `bitshares-ui` repository in the github `bitshares` organization.
