---
title: Hack the DEX Incident Report - 004
layout: announcement
---
### Unhandled Exception of asset_settle_operation

On December 6th 2018 the [Hack the DEX](https://hackthedex.io) Team received a report of a potential 
unhandled exception that would result in halting the blockchain. The report was evaluated, tested, 
patched and code was distributed to block producing nodes on December 8, 2018. The BitShares network 
was **not** impacted, **no** user funds were affected and **all operations continue to function** as
designed. 

### Reward
Special thanks to [@cogutvalera](https://github.com/cogutvalera) for providing the research and 
prototype code to resolve the bug. The Hack the DEX Team evaluated the submission and awards 
**15,000 bitUSD** tokens as a reward for disclosing the bug.

### Root Cause
An unhandled exception existed allowing a user to force-settle an asset which would result in a 
payment greater than GRAPHENE_MAX_SHARE_SUPPLY. The execution of a forced settlement happens at a 
specific time after the user requested it through an `asset_settle_operation`. In very specific cases, 
this execution would run into an assertion failure, which would prevent any additional blocks from 
being applied to the chain database, which would effectively halt the chain.

### Resolution
A _soft fork_ was distributed to block producing nodes by the BitShares Core Team, which prevents the 
issue from entering the blockchain. A permanent fix is in the making, see 
[Pull Request #1498](https://github.com/bitshares/bitshares-core/pull/1498). The soft fork currently 
prevents certain forms of `call_order_update_operation` from being included in proposals. This 
restriction will be removed when the permanent fix is activated at the time of the upcoming 
[Protocol Upgrade Release](https://github.com/bitshares/bitshares-core/projects/10).


### Acknowledgement

The BitShares Blockchain Foundation would like to thank the Hack the DEX Team and Core Team developers 
for their quick response time and resolving the bug in a timely and secure manner.

### Announcement Mailing List

In order to improve responsiveness, the BitShares Blockchain Foundation has set
up several mailing lists including a low noise `critical` and an `announcement`
list that we recommend fundamental industry partners (like exchanges and money
transmitting partners) to [subscribe to](http://lists.bitshares.foundation).
This will enable all businesses in the BitShares network to be aware of all
latest developments.
