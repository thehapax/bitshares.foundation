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
status:
  proposal-vetted: True
  worker-created: False
  worker-approved: False
  worker-paying: False
  worker-finished: False
discussions:
 - name: Bitshares Talk
   url: <placeholder>
 - name: steemit/@sc-steemit
   url: https://steemit.com/bitshares/@sc-steemit/placeholder
payments:
price: up to $437,565 (¥2,917,100)
duration: 46 weeks
start: 2019/02/11
end: 2019/12/29
---

# Introduction

This proposal is designed to fund the frontend development efforts for the BitShares Wallet. This
benefits the community by creating a blueprint for other individuals and organizations
interested in providing frontend functionality for the BitShares blockchain.

This worker funds a **not to exceed** budget for development of the Bitshares UI application,
according to the below details in *Table 1*.

- Transparent accounting provided by the BitShares Blockchain Foundation
- Compensation remitted in a viable SmartCoin (i.e. bitCNY)
- All accumulated and unallocated BTS returned to the Reserve Pool at the conclusion of the Worker

As the team size scales or BTS token valuations fluctuate, subsequent Worker(s) will be offered to fully fund the Intent.

*This worker proposal will supercede the remaining of 201808-bitshares-ui proposal, any funds left in the old worker will be transferred to the new worker (currently ~13k bitUSD) to cover outstanding bounties*

# Bounties

Issues located at [bitshares/bitshares-ui](https://github.com/bitshares/bitshares-ui/issues)
will be gathered into milestones containing work over two week GitHub sprints.
Anyone in the community will be able to claim, work and submit a PR for
that issue. If the PR is accepted, the user will be paid according to
the terms on the [README.md](https://github.com/bitshares/bitshares-ui/blob/develop/README.md)
under the Development Process heading. Bounties are paid at a rate of $125/hr.

This worker will, as before, continue to support [Beet](https://github.com/bitshares/beet) development within the workers coding bounty system. Beet is a stand-alone key/identity-manager and signing app for BitShares, heavily influenced by Scatter. 

# Prioritization

There are many opinions across the BitShares community about what is
most important. These opinions vary due to the broad range of individual
capabilities. Some users want to see new features developed as soon as
possible while others would like to see a refined user interface with
reliable, less ambiguous controls and helpful documentation. It's our
goal as a team to listen to everyone and make decisions based upon what
we hear from the community.

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

This worker proposal will continue to enhance this effort by:

* Creating a more modular exchange experience.
* Migrate to ANT components complete with a style guide.
* Further refine the navigation moving away from the sub-tab model.
* Create an easy way for exchanges to brand their own wallet from the reference wallet.
* Establish a more methodical QA and testing phase before releasing each version.
* Create a series of automated front and backend tests to reduce resurfacing bugs.

# Team

#### Table 1. Bitshares UI Team Effort Budget (Weekly)

Roles|Rate (USD)|Team Member|Estimated Hours
-|-|-|-
Project Manager (1)|$125/hour|Magnus Anderson|9 hours weekly
UX Coordinator (1)|$125/hour|Ihor Brazhnichenko|7 hours weekly
Release Management (1)|$125/hour|Stefan Schiessl|9 hours weekly
Funds and Sprint Management|$125/hour|Alex M|4 hours weekly
**TEAM EFFORT**|&nbsp;|&nbsp;|29 hours weekly
**$3,625 WEEKLY**|&nbsp;|&nbsp;|&nbsp;
-|&nbsp;|&nbsp;|&nbsp;
Community Claims: (2)|&nbsp;|&nbsp;|&nbsp;
-- Code Bounty|$125/hour|-open-|25 hours weekly
-- UX Bounty|$125/hour|-open-|15 hours weekly
**BUDGET FOR CLAIMS**|&nbsp;|&nbsp;|40 hours weekly
**$5,000 WEEKLY**|&nbsp;|&nbsp;|&nbsp;

*(1) unused hours will be designated to coding bounties.*

*(2) Bounty hours includes both [bitshares-ui](https://github.com/bitshares/bitshares-ui) and [beet](https://github.com/bitshares/beet) GitHub projects.*

#### Table 2. Bitshares UI Team Travel Expeses (Once)

Description | Amount 
--|--:
Travel Budget (Graphene specific conferences) | USD 20,000
**Total USD** | $20,000
**Total (CNY EQUIVALENT)** | **¥133,300**

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

# Development Cost

Currently, updates to the BitShares-ui are handled by a small team of 
users who are claiming issues and being paid bounties on these issues. 
The only exceptions to this are Magnus Anderson, Stefan Schiessl, 
Ihor Brazhnichenko and Alex M, who are each paid a flat rate to manage issues, 
code review and other project duties respectively. Unused hours should 
primarily be used for issues work.

Fixed positions hours will be reported transparently togehter with invoices.

Furthermore, the BitShares Blockchain Foundation seeks a
management fee (&lt;5%) for dealing with the on-chain worker proposal and
offer transparent accounting.

A one-time fixed travel budget expense is included to reimburse developers 
for expenses to Graphene specific conferences according to guidlines.

#### Table 3. UI Team Budget

Role|Amount (Period)|As Daily|TOTAL BUDGET
--|--|--|--:
Total Team Roles (Table 1)|$3,625 (weekly)| ~$517,85 |&nbsp;
Total Community Claims (Table 1)|$5,000 (weekly)| ~$715 |&nbsp;
Travel Expeses (Table 2)| $20,000 (once) | ~$60.8 |&nbsp;
-| &nbsp; | &nbsp; | &nbsp; 
Escrow Fee 5% (BBF) | $452.5 (weekly) | ~$60.8 | $20,815 
++ Daily Budget | &nbsp; | $1,359 | &nbsp; 
**TOTAL 46 WEEK BUDGET USD** | &nbsp; | &nbsp; |**$437,565**
**TOTAL 46 WEEK BUDGET (CNY EQUIVALENT)** | &nbsp; | &nbsp; | **¥2,917,100**

# Duration and Pay

**Duration:** This proposal will last for 46 weeks, starting from 11th Febrary 2019, ending on 29th December 2019.

**Transparent Accounting:**
- Funds Manager will review and approve submitted time sheets, then forward invoices to BitShares Blockchain Foundation for release of funds from escrow to contributor's account
- Funds Manager will review and approve vendor invoices, then forward to BitShares Blockchain Foundation for direct payment to vendor

**Devaluation Multipler**: This Worker introduces a devaluation multiplier to mitigate the impacts of a depreciating BTS token during the active period. We propose to protect against prolonged BTS devaluation of approximately one-third (-20%) by using a 1.25 devaluation multiplier. Initially, BTS will be accumulated at rate 125% of the required daily budget. The BBF will use the accumulated BTS to purchase bitCNY from the market, up to the UI Team Budget detailed above in Table 1.

**Calculations (as of 27 JAN 2019):**
- 6.75 = USD/CNY foregin exchange rate
- 3.93824 = bitCNY/BTS price feed
- 1.25 = Devaluation multiplier to mitigate market fluctuations
- 45,158 BTS/day ≈ $1,359 USD/day * 6.75 USD/CNY * 3.93824 bitCNY/BTS * 1.25 devaluation multiplier

**Payments**: All payments are converted from USD and remitted in bitCNY with method developed by the BitShares Blockchain Foundation.

=======

* Feature - Adding functionality to the BitShares UI that previously didn't exist.
* Proposed Feature - A potential feature that requires further discussion.
* Task - Time commitment (improving the look of a table might be considered a task)
* Bug - Resolving something that is broken
* Duplicate - Consolidating multiple similar requests into a single issue
* Invalid - An issue that is not desired by the community or is
  technically out of reach or ambiguous