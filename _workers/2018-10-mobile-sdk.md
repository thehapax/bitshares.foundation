---
language: en
layout: worker
type: budget
bfid: 201811-mobile-sdk
workerid:
title: OpenSource BitShares Mobile SDK (android/ios)
name: Blockchain Projects BV
company:
 name: Blockchain Projects BV
 url: http://blockchainprojectsbv.com
discussions:
 - name: bitsharestalk
   url:
 - name: steemit
   url:
price: up to 100,000 €/bitEUR
duration: 12 months
start: 2018/11/15
end: 2019/12/31
paymentaccount: blockchain-bv
---

# Intent

Over the last months, we at Blockchain Projects have seen a lot of demand for mobile applications running on top of
BitShares and allowing to use tokens. The desire to have a mobile application capable of transacting with BitShares has
motivated us to start development long ago.

What is not widely known is that we already have a mobile application framework for BitShares that allows to develop and
customized a variety of mobile apps for the BitShares Blockchain. Among this, we have developed what is needed to
provide UIA support for loyalty (or similar) program with sponsoring and promotion screens and listings and a KYC
registration framework.

This framework, or Software Development Kit (SDK) is **highly customizable**, allows for company-specific **branding**
and is built entire using React-native/redux - a widely known framework that **supports Android as well as iOS**.

Along the publishing of this worker proposal, we release the majority of the software open source for the entire
community to use according to the GPL license. The worker proposal requests funding from the BitShares Blockchain to
continue development of this Framework/App for the next 12 months.

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

This worker delivers, in case it is accepted by the community, the sources of a fully functional mobile wallet
development toolkit that builds to a mobile wallet app today.

The community will be free to leverage this software delivery to build their own products based on this framework, such
as the usual UIA use-cases: Remittance, Loyalty programs, service coins, prepaid cards etc.

Our delivery focuses on:
* code improvements
* unit testing
* basic UI/UX
* toolchaining for Android and iOS
* continuous integration and testing
* technical documentation

for the mobile framework code base.

# Milestones/Delivery and Costs

Provided that the code is at a stable state today, we are asking for a budget of **up to 100k€** to fund development
resources **for 12 months**. The budget accounts for the following roles and management

| Roles                          | Rate (bitEUR/h)  | 
| ------------------------------ | ---------------: | 
| Full-stack Developer           | €130.00          | 
| Architecture                   | €80.00           | 
| QA and Testing                 | €70.00           | 
| HTML/CSS Developer             | €70.00           | 
| Designer                       | €50.00           | 

| Purpose                        | Rate (bitEUR)    | 
| ------------------------------ | ---------------: | 
| Management Fee                 | €1500/mth        | 
| Code review                    |  €500/mth        | 
| Escrow Fee (BBF)               | 5%/€500 (total)  |

The character of this worker proposal is towards developing a framework for mobile development (an SDK).
Consequently, an exemplary mobile wallet will be provided for testing but applying for "app-stores" inclusion for
a branded wallet is not covered by this proposal.

# Fineprint

* This worker pays in **bitEUR/€** instead of bitUSD/$
* The Terms & Conditions of Blockchain Projects BV apply with the BitShares DAC being referred to as Client
* Blockchain Projects BV to perform and assist with delivery and coordination
* Blockchain B.V. owns the IP and will grant an open source license
* The code will moved into the bitshares organizations according to the terms of the bitshares github organization
* ^1: The "BitShares-UI team" being the team working on the `bitshares-ui` repository in the github `bitshares` organization.
