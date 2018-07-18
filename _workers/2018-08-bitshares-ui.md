---
layout: worker
bfid: 201808-bitshares-ui
workerid:
title: BitShares UI Team
name: Bill Butler
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
payments:
price: up to 290,000$
duration: 8 months
start: 2018/08/01
end: 2019/03/31
---

# Introduction

The BitShares GUI has a great deal of functionality, so much that it can
be overwhelming for new users to grasp. Some users expect it to simply
hold their funds securely and allow for transfers while others require
the full power of the exchange, voting, asset creation etc.

The goal of assembling this team is to better understand the various use
cases for BitShares and, based upon that information, craft an improved
user experience.

# Bounties

Issues located at
[bitshares/bitshares-ui](https://github.com/bitshares/bitshares-ui/issues)
will be gathered into Milestones with a two week release schedule.
Anyone in the community will be able to claim, work and submit a PR for
that issue. If the PR is accepted, the user will be paid according to
the terms on the
[README.md](https://github.com/bitshares/bitshares-ui/blob/bitshares/README.md)
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

# Development Cost

Currently, updates to the bitshares-ui are handled by Sigve Kvalsvik
(@svk). We have included the BitShares Blockchain Foundation on this
proposal in order to increase the surface area for code review, testing
and acceptance as well as facilitate payments in bitUSD. This proposal
is intended to alocate a budget for making improvements to the BitShares
client and establish a more formal and ongoing effort towards the
development effort.

Currently, updates to the BitShares-ui are handled by a small team of 
users who are claiming issues and being paid bounties on these issues. 
The only exceptions to this are Bill Butler, Sigve Kvalsvik and Magnus
Anderson who are each paid a flat rate to manage issues and code review
respectively. Furthermore, the BitShares Blockchain Foundation seeks a
management fee (<10%) for dealing with the on-chain worker proposal and
offer transparent accounting.

* Monthly

Role|Amount(USD)
--|--:
Coordination / Funds Distribution | $3,000
Project Manager | $4,500
Code Review / Releases | $4,500
UX/UI Bounty | $8,000
Coding Bounty | $12,000
Bitshares Blockchain Foundation | $3,000
Total Monthly | $35000

* Fixed Expenses

Description | Amount(USD)
--|--:
Travel Budget (Graphene specific conferences) | $10,000

# Team

## Sigve Kvalsvik

* Role: React Dev, Release Management, Code Review
* Development Experience: Maintainer of BitShares-UI for a long time
  already, funded by multiple workers previously, creator of
  bitsharesblocks.com during BitShares 1, long-term member and developer
  in the bitshares community, maintainer of bitsharesjs.
* Platforms / Languages: NodeJS, React, Angular, and others

 
## Magnus Anderson (startail)

* Role: Project Manager
* Crypto Experience: 5 years of trading and using, 3 years of community
  building, 2 years of DPOS Node Maintainer
* Development Experience: 20 years of webside development in various
  forms, 15 years of sever management, 4 years of Git experience
* Languages: PHP, jQuery, mySQL, HTML, Javascript, React, Python, Bash,
  many more

Duties include the grooming and prioritization of all issues (15 hours per week).
Milestones will be created for each 2 week Sprint. Sprints will be
populated with enough issues to occupy 90 hours for the 2 week sprint.
Each issue will be tagged as feature / task / bug / duplicate / rejected, estimated,
and assigned to developers who request the work.

## Bill Butler

* Role: Issue coordination and funds tracking and distribution
* Crypto Experience: 4 years, BTC, LTC, PTS, BTS 1.0/2.0, STEEM, PPY.
  Helped manage github issues a couple of years ago. Worked with svk.
* Development Experience: Founded an ISP in 1993. NodeJS, Angular, PHP,
  CouchDB, SQL. UX/UI Experience. VP Engineering for a healthcare
  software development firm. Eight years experience managing development
  teams.
  
Duties include overseeing the hourly assignments for issues, creating milestones,
communicating with the project manager to ensure priorities are met and collecting
and distributing funds to contributors in a timely manner.

* Feature - Adding functionality to the BitShares UI that previously didn't exist.
* Proposed Feature - A potential feature that requires further discussion.
* Task - Time commitment (improving the look of a table might be considered a task)
* Bug - Resolving something that is broken
* Duplicate - Consolidating multiple similar requests into a single issue
* Invalid - An issue that is not desired by the community or is
  technically out of reach or ambiguous
