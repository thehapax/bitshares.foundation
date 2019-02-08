---
layout: worker
language: en
bfid: 201902-bitshares-ui
type: budget
workerid: 1.14.xxx
title: BitShares UI Team
name: Magnus Anderson
company:
  name:
  url:
status: draft
discussions:
 - name: Bitshares Talk
   url: <placeholder>
 - name: steemit/@sc-steemit
   url: https://steemit.com/bitshares/@sc-steemit/placeholder
payments:
price: up to $437,587.5 (~¥2,953,715)
duration: 46 weeks
start: 2019/02/11
end: 2019/12/29
---

# Introduction

The BitShares UI (also known as reference UI) has a great deal of functionality, so much that it can be overwhelming for 
new users to grasp. 
Some users expect it to simply hold their funds securely and allow for transfers and trading, 
while others require the full power of the blockchain, e.g. for voting, asset management, permissions and 
multi-sig configuration, black and whitelisting, proposal creation and direct debit mandates.

The goal of this worker is to build out the reference UI to hightlight all the features that the blockchain provides
and tackle one of the root problems in terms of connectivity and reliability of the UI.

**Remark 1**
There was a personel shift in the team of the BitShares UI. Bill Butler has decided to leave the UI worker and pass 
the hat on to Magnus Anderson (@startail), who will be stepping up to the role of general project manager. Additionally, Alex M (@clockwork) will be assisting with issue and fund management.

**Remark 2**
The previous UI worker had a purely decentralized approach for development, which basically was: 
Anything can be worked on by anyone at anytime. That had its perks, but also was inefficient in other areas.
This new worker is restructured and moves a bit away from that for the team in order to enforce a tighter schedule
to achieve key aspects of the development.

# Bounties

Issues that are in scope (see subsection below)
will be gathered into milestones containing work over two week GitHub sprints.
Those issues will be prioritized like indicated below, anyone in the community will be 
able to claim, work and submit a PR for
that issue. If the PR is accepted, the user will be paid according to
the terms on the [README.md](https://github.com/bitshares/bitshares-ui/blob/develop/README.md)
under the Development Process heading. Bounties are paid at a rate of up to 125 USD/hour.

In contrast to the previous worker, the immediate team mentioned in this proposal must work on high priority issues 
first. This prioritization of issues is done by the team as well and is meant as a self-control measure and to allow to pursue a defined roadmap.
There have been cases in the past that important issues are being postponed simply because no one worked on them. And that 
is unacceptable.

## Scope

The main repositories covered through this worker are the following (others may be addded if suitable)
 - https://github.com/bitshares/bitshares-ui
 - https://github.com/bitshares/bitshares-ui-style-guide
 - https://github.com/bitshares/bitsharesjs
 - https://github.com/bitshares/bitsharesjs-ws

This worker will, as before, continue to support [Beet](https://github.com/bitshares/beet) development within 
the workers coding bounty system. Beet is a stand-alone, multi-chain key/identity-manager and signing app for BitShares
and is found in 
 - https://github.com/bitshares/beet
 - https://github.com/bitshares/beet-js

# Prioritization

There are many opinions across the BitShares community about what is
most important. These opinions vary due to the broad range of individual
capabilities. Some users want to see new features developed as soon as
possible while others would like to see a refined user interface with
reliable, less ambiguous controls and helpful documentation. It's our
goal as a team to listen to everyone and make decisions based upon what
we hear from the community.

The team will pursue to ruther the UI in the following aspects

* Refactoring core connectivity and reliability components.
* Establish a more methodical QA and testing phase before releasing each version.
* Create a series of automated front and backend tests to reduce resurfacing bugs.
* Finish migration to ANT components complete with a style guide.
* Further refine the navigation moving away from the sub-tab model.
* Creating a more modular exchange experience and an easy way for exchanges to brand and configure their own.

In addition to that, all community feedback will be considered and groomed into issues where feasible. 

## Bugs

Bugs fixes represent the top priority for the UI Team and are worked first
to ensure the Bitshares application meets our users' expectations.

## Low Hanging Fruit

This represents features or tweaks that add give the application a lot
of bang for very little effort. By focusing on low hanging fruit, we can
drastically improve the UI for many people very quickly and cross these
items off the todo list.

## Application Consistency

Tables, dropdowns, form fields, modals, fonts, icons, colors. To date
we have invested a great deal of time streamilining the UI experience.
Our past efforts have sought to improve the overall look and feel and
have attempted to group similar functions. We recognize there is still
room for improvement.

## New features

The BitShares core is ever evolving and anything new that comes out of it will need to be reflected in the UI as well.

# Team

## Magnus Anderson (@startail)

* Role: Project Manager
* Main Duties: Team leader, issues grooming, UI/UX Coordination etc.
* Crypto Experience: 6 years of trading and using, 4 years of community
  building, 3 years of DPOS Node Maintainer
* Development Experience: 20 years of webside development in various
  forms, 15 years of sever management, 5 years of Git experience
* Languages: PHP, jQuery, mySQL, HTML, Javascript, React, Python, Bash,
  many more

Duties include grooming and prioritization of all issues and
UI/UX cooridnation together with UX coordinator.

Milestones will be created for each 2 week Sprint. Sprints will be
populated with enough issues to occupy 80 hours for the 2 week sprint.
Each issue will be tagged as feature / task / bug / duplicate / rejected, estimated,
and assigned to developers who request the work.

## Ihor Brazhnichenko (@gibbsfromncis)

* Role: UX Coordinator
* Main Duties: Coordinate UX together with developers, locate and introduce new potential UX developers.
  Communicating with the project manager to ensure priorities are met.
* Development experience: 8 years of professional front-end development, 5 years of team management, 
  strong UI/UX eye. Different kinds of projects: IoT Platform for managing 100,000 online devices across the world, 
  real-time online games, a portal for infrastructure management for communications network company that 
  transmits radio and TV programmes, popular food delivery service.  
* Languages: JavaScript, Node.js, PHP, Go, Java, React, Vue, Angular, and many more

## Blockchain Projects BV (Stefan Schiessl)

* Role: Release Management
* Main Duties: Code review for submitted PRs and coordinate new releases
* Development Experience: Maintainer of BitShares UI, strong applied mathematics background and developing and managing software development since 2005, for crypto since 2017
* Languages: NodeJS, React, and others
* https://www.blockchainprojectsbv.com/

## Alex M (@clockworkgr)
* Role: Funds and Sprint Management
* Main Duties: Summarize and report development hours collecting 
  and distributing funds to contributors in a timely manner.
* Development Experience: Over 16 years web-development experience in both front-end and back-end. 
  Been involved in BitShares development since the beginning of 2018. Maintainer of Beet. 
  Current BitShares witness & committee member.

# Budget

Budget includes development costs for bounties and the fixed positions of the team as well as a travel budget for 
conferences. Furthermore, the BitShares Blockchain Foundation seeks a management fee of 5% of paid invoices for 
dealing with the on-chain worker proposal, providing a legal framework and offer transparent accounting.

#### Table 1. Bitshares UI Team Fixed Positions (Weekly)

The hours of the fixed positions will be reported transparently together with invoices.

Roles|Rate (USD)|Team Member|Estimated Hours
-|-|-|-
Project Manager (1)| 125 USD/hour|Magnus Anderson|9 hours weekly
UX Coordinator (1)| 125 USD/hour|Ihor Brazhnichenko|7 hours weekly
Release Management (1)| 125 USD/hour|Stefan Schiessl|9 hours weekly
Funds and Sprint Management (1)| 125 USD/hour|Alex M|4 hours weekly
**TEAM EFFORT**|&nbsp;|&nbsp;|29 hours weekly
-|&nbsp;|&nbsp;|&nbsp;
Bounties: (2)|&nbsp;|&nbsp;|&nbsp;
-- Code and UX | up to 125 USD/hour|-open-|40 hours weekly
**BUDGET FOR BOUNTIES**|&nbsp;|&nbsp;|40 hours weekly

 - *(1) Unused hours will be designated to coding bounties that are defined by the team in pursuit of key improvements of the UI*
 - *(2) Bounty hours include issues in any of the repositories listed in scope. At the moment all issues are treated equal, but we reserve the right to adjust hourly pay depending on the task. Any change would be clearly indicated in the Contributing Guidelines and the issue*

#### Table 2. Bitshares UI Team Travel Expeses (Once)

A one-time fixed travel budget expense is included to reimburse developers 
for expenses to suitable conferences according to travel expenses guidelines of the BBF.

Description | Amount 
--|--:
Travel Budget | up to 20,000 USD

#### Table 3. Summary

Role | Amount (Period)
--|--:
Team Roles (Table 1)| 3,625 USD (weekly)
Community Claims (Table 1)| up to 5,000 USD (weekly)
Travel Expeses (Table 2)| up to 20,000 USD (once)
-| &nbsp; | &nbsp;
Total Budget | up to 416,750 USD (46 weeks)
Escrow Fee 5% | up to ~452 USD (weekly) 
-| &nbsp; | &nbsp; 
**TOTAL ASKING** | **437,587.5 USD** (46 weeks)
equivalent (6.75 CNY/USD) | **2953715.625 CNY** (46 weeks)

**Remark**

- This worker funds a **not to exceed** budget for development according to *Table 3*.
- Transparent accounting provided by the BitShares Blockchain Foundation
- Compensation remitted in a viable SmartCoin (i.e. bitCNY)
- All accumulated and unallocated BTS returned to the Reserve Pool at the conclusion of the Worker

As the team size scales or BTS token valuations fluctuate, subsequent Worker(s) will be offered to fully fund the Intent.

# Duration and daily BTS pay

**Duration:** This proposal will last for 46 weeks, starting from 11th Febrary 2019, ending on 29th December 2019.

**Transparent Accounting:**
- Funds Manager will review and approve submitted time sheets, then forward invoices to BitShares Blockchain Foundation for release of funds from escrow to contributor's account
- Funds Manager will review and approve vendor invoices, then forward to BitShares Blockchain Foundation for direct payment to vendor

**Devaluation Multipler**: This Worker introduces a devaluation multiplier to mitigate the impacts of a depreciating BTS token during the active period. We propose to protect against prolonged BTS devaluation of approximately one-third (-20%) by using a 1.25 devaluation multiplier. Initially, BTS will be accumulated at rate 125% of the required daily budget. The BBF will use the accumulated BTS to purchase bitCNY from the market, up to the UI Team Budget detailed above in Table 1.

**Calculations (as of 27 JAN 2019):**

Type | Value
--|--:
USD/CNY foreign exchange rate | 6.75
bitCNY/BTS | 3.93824
Devaluation multiplier to mitigate market fluctuations | 1.25
Total asking USD | 437,587.5
Worker duration | 46 weeks
bitCNY peg | 1:1

The daily BTS payout is calculated as follows

    45,156 BTS/Day ≈ 437,587.5 USD / (46*7 Days) * 6.75 CNY/USD * 1 bitCNY/CNY * 3.93824 BTS/bitCNY * 1.25

**Payments**: All payments are converted from USD and remitted in bitCNY, converstion rates will be visible in invoices through the accounting provided by BitShares Blockchain Foundation.
