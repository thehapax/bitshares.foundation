---
layout: worker
bfid: 201708-bitsharesui
workerid: 1.14.58
title: BitShares UI Team
name: Bill Butler
company:
  name:
  url:
status:
  proposal-vetted: True
  worker-created: True
  worker-approved: False
  worker-paying: False
  worker-finished: False
discussions:
 - name: steemit/@billbutler
   url: https://steemit.com/bitshares/@billbutler/bitsharesui-worker-proposal-1-14-58
payments:
price: 150,000$
duration: 6 months
start: 2017/08/15
end: 2018/02/15
---

# Introduction

The BitShares GUI has a great deal of functionality, so much that it can
be overwhelming for new users to grasp. Some users expect it to simply
hold their funds securely and allow for transfers while others require
the full power of the exchange, voting, asset creation etc.

The goal of assembling this team is to better understand the various use
cases for BitShares and, based upon that information, craft an improved
user experience.

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

## Low Hanging Fruit

This represents features or tweaks that add give the application a lot
of bang for very little effort. By focusing on low hanging fruit, we can
drastically improve the UI for many people very quickly and cross these
items off the todo list.

## Application Consistency

Tables, dropdowns, form fields, modals, fonts, icons, colors. We plan to
seek community comment via github issues and mock ups to propose
consistent ways to view all of the current information available in the
BitShares Wallet.

In some cases, this simply means we will alter a table to fit into an
accepted style. We may propose to merge two separate views into one if
it's discovered that they contain related information. Along the way,
the goal is to create a flow that most people will find intuitive.

## Documentation

We have a goal to ensure that most features in the BitShares wallet are
intuitive with additional guides and information available for those who
need additional assistance.

# Development Cost

Currently, updates to the bitshares-ui are handled by Sigve Kvalsvik
(@svk). We have included the BitShares Foundation on this proposal in
order to increase the surface area for code review, testing and
acceptance as well as facilitate payments in bitUSD. This proposal is
intended to increase the budget for making improvements to the BitShares
client and establish a more formal and ongoing effort towards the
development effort. If successful, our hope is that the improvements
will 

1. enhance the experience for existing users
2. streamline the existing on-boarding and funding pathways for new users
3. set a precedent for the method of reporting issues
4. establish a release timeline with issues and milestones
5. manage the communication process w.r.t. why some features are accepted and others are not
6. establish automated tests to decrease the likelihood of returning bugs.

# Team

## Sigve Kvalsvik

* Role: React Dev, Release Management, Code Review
* Development Experience: Maintainer of BitShares-UI for a long time
  already, funded by multiple workers previously, creator of
  bitsharesblocks.com during BitShares 1, long-term member and developer
  in the bitshares community, maintainer of bitsharesjs.
* Platforms / Languages: NodeJS, React, Angular, and others

 
## Calvin Froedge

* Role: React Dev
* Crypto Experience: Lots of trading / holding activity. Lots of
  purchasing goods / services with crypto. 
* Development Experience: Maintainer for private SDK (angular) which
  powers widget on 300k websites serving 500m users. Architected and
  implemented complex excel-like product for commercial real estate
  management with full support for excel keyboard bindings and many custom
  controls.
* Platforms / Languages: NodeJS, React, Angular, Python, PHP, many others

## Bill Butler

* Role: Agile Project Manager and UI/UX moderator
* Crypto Experience: 3 years, BTC, LTC, PTS, BTS 1.0/2.0, STEEM, PPY.
  Helped manage github issues a couple of years ago. Worked with svk.
* Development Experience: Founded an ISP in 1993. NodeJS, Angular, PHP,
  CouchDB, SQL. UX/UI Experience. VP Engineering for a healthcare
  software development firm. Eight years experience managing development
  teams.

As the project manager for bitshares/bitshares-ui, I will review all
issues created (15 hours per week). I will also create UX and UI mockups
and mediate discussions on github around new features (Example).
Milestones will be created for each 2 week Sprint. Sprints will be
populated with enough issues to occupy 90 hours for the 2 week sprint.
Understand that these hours are quality hours, not planning hours. As
many in this field are aware, developers are always working on problems
in their minds. In most cases I've found that a 15 hour task will
require anywhere from 25 - 30 hours of a developer's time. Each issue
will be tagged as feature / task / bug / duplicate / rejected. 

* Feature - Adding functionality to the BitShares UI that previously didn't exist.
* Proposed Feature - A potential feature that requires further discussion.
* Task - Time commitment (improving the look of a table might be considered a task)
* Bug - Resolving something that is broken
* Duplicate - Consolidating multiple similar requests into a single issue
* Invalid - An issue that is not desired by the community or is technically out of reach or ambiguous
