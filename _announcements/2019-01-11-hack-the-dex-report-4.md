---
title: Hack the DEX Incident Report - 004
layout: announcement
---
### Halt Chain by Global Settlement of Short Asset with Supply Greater Than GRAPHENE_MAX_SHARE_SUPPLY

On December 6th 2018 the [Hack the DEX](https://hackthedex.io) Team received a report of a potential 
unhandled exception that would result in halting the blockchain. The report was evaluated, tested, 
patched and code distributed block producing nodes on December **TODO: XX**, 2018. The BitShares 
network was **not** impacted, **no** user funds were affected and **all operations continue to function**
as designed. 

### Reward
Special thanks to [@cogutvalera](https://github.com/cogutvalera) for providing the research and 
prototype code to resolve the bug. The Hack the DEX Team evaluated the submission and awards 
**TODO: XX,XXX bitUSD** tokens as a reward for disclosing the bug.

### Root Cause
An unhandled exception existed where, at the time an asset entered global settlement, an asset with a 
supply greater than GRAPHENE_MAX_SHARE_SUPPLY would cause **TODO: a very technical description**. 

### Resolution
The Core Team created a patch to handle the above condition and fail gracefully. The patch was 
distributed to the active block producers for implementation. The code relevant code changes maybe 
found **TODO: update URL** [here](https://github.com/bitshares/bitshares-core/commit/ZZZZZZZZZZZZZZ). 
This code will be included within next Release.

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
