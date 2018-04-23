---
language: en
layout: worker
type: budget
bfid: 2018-02-bitsharesui
workerid: 1.14.83
title: BitShares UI Team
name: Bill Butler
company:
  name:
  url:
status: paying
discussions:
 - name: steemit/@billbutler
   url: https://steemit.com/bitshares/@billbutler/bitshares-gui-worker-proposal-renewal
 - name: bitsharestalk
   url: https://bitsharestalk.org/index.php/topic,25903.msg315544.html
payments:
 - date: 2018/03/05
   oid: 1.11.148465311
   amount: 17,718.75 bitUSD
 - date: 2018/03/16
   oid: 1.11.155339391
   amount: 11,668.75 bitUSD
 - date: 2018/04/03
   oid: 1.11.164334127
   amount: 13,468.75 bitUSD
 - date: 2018/04/23
   oid: 1.11.175203741
   amount: 14,056.25 bitUSD
paymentaccount: bitshares-ui
invoices:
 - 201802-bitsharesui-Sprint-180302.xlsx
 - 201802-bitsharesui-Sprint-180315.xlsx
 - 201802-bitsharesui-Sprint-180401.xlsx
 - 201802-bitsharesui-Sprint-180418.xlsx
price: $210,000
duration: 6 months
start: 2018/02/15
end: 2018/08/15
redirect_from: 
 - /worker/budget/2018-02-bitshares-ui
---

# Introduction

The BitShares GUI has a great deal of functionality, so much that it can
be overwhelming for new users to grasp. Some users expect it to simply
hold their funds securely and allow for transfers while others require
the full power of the exchange, voting, asset creation etc.

The goal of this worker proposal is to build upon the progress of the
past years improvements to the UI.

Being a budget worker, the price tag is an upper bound for the costs
that this worker proposal can have at most. Funds are used on a
cost-basis and are accounted for hourly. After termination of the
worker proposal, unused funds are given back to the BitShares DAC.

# Bounties

Issues located at
[BitShares/BitShares-ui](https://github.com/BitShares/BitShares-ui/issues)
will be gathered into Milestones with a two week release schedule.
Anyone in the community will be able to claim, work and submit a PR for
that issue. If the PR is accepted, the user will be paid according to
the terms on the
[README.md](https://github.com/BitShares/BitShares-ui/blob/master/README.md)
under the Development Process heading.

# Prioritization

There are many opinions across the BitShares community about what is
most important. These opinions vary due to the broad range of individual
capabilities. Some users want to see new features developed as soon as
possible while others would like to see a refined user interface with
reliable, less ambiguous controls and helpful documentation. It's our
goal as a team to listen to everyone and make decisions based upon what
we hear from the community.

## Bugs

At the core, we plan to start with bugs. Bugs cause unexpected behavior
and unexpected behavior is particularly vexing with a financial
application.

## Responsive Design

In the past 6 months, the UI team has improved the usability of the
BitShares wallet in desktop mode, but the performance on the mobile view
has suffered. We have allocated additional funds with this worker to 
invest in responsive design. It will be a priority to invest in work that
makes useability on small screens enjoyable.

## Application Consistency

Tables, dropdowns, form fields, modals, fonts, icons, colors. We plan to
seek community comment via github issues and mock ups to propose
consistent ways to view all of the current information available in the
BitShares wallet.

In some cases, this simply means we will alter a table to fit into an
accepted style. We may propose to merge two separate views into one if
it's discovered that they contain related information.

## UX/UI

Along the way, the goal is to create a flow that most people will find intuitive.
The additional funding for this proposal will add weight to the UX/UI
design work that needs to happen up front. This new budget proposal earmarks
$8,000 per month to the UX process alone.

## Documentation

We have a goal to ensure that most features in the BitShares wallet are
intuitive with additional guides and information available for those who
need additional assistance.

## Budget

Currently, updates to the BitShares-ui are handled by a small team of
users who are claiming issues and being paid bounties on these issues.
The only exceptions to this are Bill Butler and Sigve Kvalsvik who are
both paid a flat rate to manage issues and code review respectively.
Furthermore, the BitShares Blockchain Foundation seeks a management fee
(<10%) for dealing with the on-chain worker proposal and offer
transparent accounting.

- Monthly

Role | Amount (USD)
--- | ---:
Project Manager | 7,500
Code Review/Releases | 4,000
UX/UI Bounty | 8,000
Coding Bounty | 12,500
BitShares Blockchain Foundation | 3,000
Total | 35,000


1. Enhance the experience for existing users
2. Streamline the existing on-boarding and funding pathways for new users
3. Set a precedent for the method of reporting issues
4. Establish a release timeline with issues and milestones
5. Manage the communication process w.r.t. why some features are accepted and others are not
6. Establish automated tests to decrease the likelihood of returning bugs

# Team

## Sigve Kvalsvik

* Role: React Dev, Release Management, Code Review
* Development Experience: Maintainer of BitShares-UI for a long time
  already, funded by multiple workers previously, creator of
  bitsharesblocks.com during BitShares 1, long-term member and developer
  in the BitShares community, maintainer of bitsharesjs.
* Platforms / Languages: NodeJS, React, Angular, and others

Will perform code review for all contributors and merge PR's into staging and handle releases on a bi-monthly schedule. This includes:

* Communicating with PR owners for change requests
* Providing hints or help for obscure endpoints
* Ensuring CI process automatically builds web and lite clients
* Ensuring versions are properly updated on BitShares.org/download

## Bill Butler

* Role: Agile Project Manager and UI/UX moderator
* Crypto Experience: 3 years, BTC, LTC, PTS, BTS 1.0/2.0, STEEM, PPY. Helped manage github issues a couple of years ago. Worked with svk.
* Development Experience: Founded an ISP in 1993. NodeJS, Angular, PHP, CouchDB, SQL. UX/UI Experience. VP Engineering for a healthcare software development firm. Eight years experience managing development teams.

As the project manager for BitShares/BitShares-ui, I will review all issues created (15 hours per week). I will mediate discussions on github around new features.
Milestones will be created for each 2 week Sprint. Sprints will be
populated with enough issues to occupy 90 hours of development work and 60 hour of UI/UX for the 2 week sprint.
Understand that these hours are quality hours, not planning hours. As many in this field are aware, developers are always working on problems in their minds. In most cases I've found that a 15 hour task will require anywhere from 25 - 30 hours of a developer's time. Each issue will be tagged as feature / task / bug / duplicate / rejected. 

* Feature - Adding functionality to the BitShares UI that previously didn't exist.
* Proposed Feature - A potential feature that requires further discussion.
* Task - Time commitment (improving the look of a table might be considered a task)
* Bug - Resolving something that is broken
* Duplicate - Consolidating multiple similar requests into a single issue
* Invalid - An issue that is not desired by the community or is technically out of reach or ambiguous
