---
title: 2.0.171025 Nodes may get stuck
layout: announcement
---

Dear readers and partners,

due to an unforeseen event, new code in the BitShares back-end, that was
supposed to only active by end of November, caused a disagreement with
block production nodes. The symptoms are a node that got stuck on
block #21,462,209.

Only nodes that updated to the new code are affected and asked to
downgrade to release tag

    2.0.171019a

In your git repository, you can run these commands:

    git fetch
    git checkout 2.0.171019a
    make

The root cause has been quickly identified and a fix is in development.
We do not expect this incident to delay the upcoming network upgrade
scheduled by end of November.


## Remark

Due to the nature of DPOS, this incident did not affect the blockchain
and its block production in a larger scale. Instead, block producers
automatically switched to backup block production being run by previous
version of BitShares core and thus keep the blockchain going.
