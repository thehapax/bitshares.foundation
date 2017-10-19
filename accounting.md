---
layout: default
permalink: /accounting
---

It is our pleasure to now publicly announce another major step for the [BitShares Blockchain Foundation](http://bitshares.foundation) towards transparency, openness and accountability.

Since we are in the fortunate position to have received sufficient trust from BitShares shareholders to successfully operate [multiple escrow workers](http://www.bitshares.foundation/worker), we feel the need to be as transparent as humanly possible to these shareholders as to how the funds are used.

Thus, we started working with an accounting system that allows us to

* treat crypto currencies properly,
* publish the accounts balances and transactions in a way that is publicly auditable, and
* ensure we properly pay our debts and pay back unnecessary funds to the BitShares reserve fund.

# Plain Text Accounting

After some research, we decided to use a [plain text accounting system](http://plaintextaccounting.org/), in particular, we are using [Ledger](http://ledger-cli.org/) - the name kind of fits :)

You can find the accounting files published on [github.com/bitshares-foundation](https://github.com/bitshares-foundation/accounting) regularly including a quick [README](https://github.com/bitshares-foundation/accounting/blob/master/README.md) that shows how to use these files properly.

Please allow us to briefly go through the tool before we show an overview of the books.

## Usage of Ledger-cli

1. Show balance of all accounts

        ledger -f ledger.ledger balance

2. Show full register

        ledger -f ledger.ledger register

2. Show register of an individual account

        ledger -f ledger.ledger register BitShares:Shareholders

## Explanations

In double-entry accounting systems, each transaction affects at least two accounts in a way that the amounts sum to zero. This means that "funds move from one account to another" while the transactions of a particular account are the actual register. This will become more clear when we go into details of the foundation's accounting.

# BitShares Blockchain Foundation Accounting

## Account Hierarchy

Let us start with first describing what accounts we are looking into and what the hierarchy of accounts looks like:

    BitSharesFoundation                  # Accounts controlled by the foundation
        bitshares.foundation             # account `bitshares.foundation`
        donations.bitshares.foundation   # account `donations.bitshares.foundation`
    BitSharesShareholders                # accounts owned by the shareholders (ultimately)
        workers.bitshares.foundation     # account `workers.bitshares.foundation`
    BitSharesReserves                    # Funds obtained from the reserves (in BTS)
    Income                               # Income for the BitShares Blockchain Foundation
        Donations                        # How much did people donate (in USD terms)
    Expenses                             # Expenses       
        TransactionFees                  # How much did we pay the network in transaction fees (in USD)
    WorkerProposals                      # Worker Proposal accounts
        Outstanding                      # How much do we "owe" escrow workers in total
        Proposals                        # How much have the workers been asking for initially

This hierarchy may be subject to change as we find more efficient ways to organize and use individual accounts.

## Escrow Worker Procedure

The procedure of dealing with a worker proposal and its payment (if the shareholders approve the worker) is as follows.

1. The worker pay is obtained through the `workers.bitshares.foundation` account which has created the workers on the blockchain to begin with.
2. Then, the BTS are traded into USD in that account.
3. Afterwards, USD are transferred into escrow by `bitshares.foundation`.
4. Freelancers that applied for the worker/job get paid through `bitshares.foundation` with bitUSD (or possibly other bitassets)

It is important to remark that funds that are in `workers.bitshares.foundation` are owned by the BitShares shareholders and not technically owned by the foundation.

In order to keep track of which worker has obtained how many BTS (in the `workers.bitshares.foundation` account), we make use of sub accounts where possible (see below). These sub accounts only appear in the accounting and are not reflected on the blockchain. After a worker has complete, we will thus be able to directly say how many BTS have been obtained from reserves, how many have been used to obtain USD and how many are to be returned to the reserves.

## Foundation Accounts

With the help of `ledger` we can give a quick summary of the accounting and individual balances. Let's dig into this real quick (state of **2017/09/29**):

```
     1       3,000 BEYONDBIT
     2      13,196.23774 BTS
     3           20.0000 CNY
     4       23,400.0000 USD  BitSharesFoundation
     5       3,196.23774 BTS
     6       23,400.0000 USD    bitshares.foundation
     7       23,000.0000 USD      201707-bsip18
     8          -0.23131 BTS
     9          400.0000 USD      201708-bitsharesui
    10       3,000 BEYONDBIT
    11      10,000.00000 BTS
    12           20.0000 CNY    donations.bitshares.foundation
    13  -1,099,749.76262 BTS  BitSharesReserves
    14    -469,333.09938 BTS    201707-bsip18
    15    -599,666.66324 BTS    201708-bitsharesui
    16     -30,750.00000 BTS    201709-steemfest
    17     578,259.29542 BTS
    18        4,219.2236 USD  BitSharesShareholders:workers.bitshares.foundation
    19     261,718.25619 BTS
    20          421.0994 USD    201707-bsip18
    21     282,879.53812 BTS
    22        3,798.1242 USD    201708-bitsharesui
    23      30,118.73689 BTS    201709-steemfest
    24          438.6994 USD  Expenses:TransactionFees
    25      -3,000 BEYONDBIT
    26     -10,000.00000 BTS
    27          -20.0000 CNY
    28       -1,000.0000 USD  Income:Donations
    29       26,812.5000 USD  WorkerProposals
    30     -152,853.5000 USD    Outstanding
    31      -23,000.0000 USD      201707-bsip18
    32       -4,000.0000 USD        chainsquad
    33      -19,000.0000 USD        cyrano
    34     -123,187.5000 USD      201708-bitsharesui
    35     -108,187.5000 USD        bitshares-ui
    36      -15,000.0000 USD        chainsquad
    37       -6,666.0000 USD      201709-steemfest:roelandp
    38      179,666.0000 USD    Proposals
    39       23,000.0000 USD      201707-bsip18
    40      150,000.0000 USD      201708-bitsharesui
    41        6,666.0000 USD      201709-steemfest
    42  --------------------
    43    -518,294.22946 BTS
    44       53,870.4230 USD
```

* **Line 1-4**: Total funds **in control** (not owned) by the bitshares blockchain foundation.
* **line 5-9**: Total funds in account `bitshares.foundation`. The BTS are for operational costs (tx fee) while the USD are separated into subaccounts for each individual worker for which the BitShares Blockchain Foundation is escrow for.
* **line 10-12**: Donations made to the bitshares blockchain foundation.
* **line 13-16**: These are the BTS that have been obtained from the BitShares reserves for each individual worker (and in total)
* **line 17-23**: Funds in account `workers.bitshares.foundation`. This account is owned by the BitShares shareholders and used to track claiming of worker pay as well as trading. There is a separation into subaccounts for each individual worker.  
* **line 24**: Transaction fees that have been paid (in USD). Technically, most of those fees occur in the workers account when creating actual workers on the blockchain.  Thus, those fees are mostly paid by BitShares shareholders.
* **line 25-28**: Total income
* **line 29**: Funds that have been paid to Worker proposals (these are separated into *Proposals* and *Outstanding*)
* **line 30-37**: Outstanding payments to approved worker proposals separated into worker proposals as well as involved entities (for worker, review, accounting, management, etc.)
* **line 38-41**: These are the funds asked for in total by all worker proposals, separated into the individual workers.

### Individual Trades

Currently, the worker account only obtains USD by buying them from the internal markets. These orders are recorded on the blockchain as well as in the off-chain books. These entries look like this:

```
2017/09/13 * Create Order for 201707-bsip18 into USD @ 10.434788520 BTS/USD
    ; 201707-bsip18        -50000.0 BTS @ 10.43479 BTS
    ; 201707-bsip18        4791.66395 USD
    workers.bitshares.foundation:201707-bsip18        -0.01213 BTS @ 0.1092 USD
    Transactionfee        (0.01213 * 0.1092 USD)

P 2017/09/13 USD 9.69688187 BTS
2017/09/13 * Trade (#20011420)
    workers.bitshares.foundation:201707-bsip18      -209.10550 BTS
    workers.bitshares.foundation:201707-bsip18      21.5642 USD @@ 209.10550 BTS
```

Here, we created an order and payed a fee of 0.01213 BTS. Later on, this order is partially filled, obtaining roughly 21 USD by paying 209 BTS. There are plenty of those fill order transactions in each of the workers' individual ledger files.

The corresponding account's registers can be obtained with

    ledger -f ledger.ledger reg workers.bitshares.foundation:201707

and looks like this

```
2017/09/13 Create Order for 201707-bsip18 into USD @ 10.434788520 BT.. BitShares:Foundation:workers.bitshares.foundation:201707-bsip18                             -0.01213 BTS                   273,166.59654 BTS
                                                                                                                                                                                                       409.5059 USD
2017/09/13 Trade (#20011420)                                           BitShares:Foundation:workers.bitshares.foundation:201707-bsip18                           -209.10550 BTS                   272,957.49104 BTS
                                                                                                                                                                                                       409.5059 USD
                                                                       BitShares:Foundation:workers.bitshares.foundation:201707-bsip18                              21.5642 USD                   272,957.49104 BTS
                                                                                                                                                                                                       431.0701 USD
```

Moving those funds into escrow is done with an entry of this type:

```
2017/09/13 * Transfering to bitshares.foundation 201707-bsip18
    workers.bitshares.foundation:201707-bsip18        -5000.0 USD
    bitshares.foundation:201707-bsip18        5000.0 USD
    workers.bitshares.foundation:201707-bsip18        -0.23131 BTS @ 0.1095 USD
    Transactionfee        (0.23131 * 0.1095 USD)
```

and results in a register entry similar to:

```
2017/09/13 Transfering to bitshares.foundation 201707-bsip18           BitShares:Foundation:workers.bitshares.foundation:201707-bsip18                          -5,000.0000 USD                   223,166.59654 BTS
                                                                                                                                                                                                       269.9826 USD
                                                                       BitShares:Foundation:workers.bitshares.foundation:201707-bsip18                             -0.23131 BTS                   223,166.36523 BTS
                                                                                                                                                                                                       269.9826 USD
```

As you can see, every action on the blockchain that affects the accounts balance, is **also recorded in our books**.

### Further Remarks

We would like to highlight a few points in what we were able to achieve in recent months:

* Proposals worth almost **180k USD** have been **approved** and are covered by the foundation
* Over **13k USD** have been paid out to freelancers already
* **700k BTS** have been claimed from the BitShares Reserves of which over **420k BTS** are unused in the currently covered workers.
* This means that **60%** of the funds in the worker account will probably be returned to the BitShares Shareholders (after the individual workers have terminated)
* **1000 USD** have been donated to `donations.bitshares.foundation`so far.
* Over **430 USD** have been paid as transaction fees of which **240 USD** are used to create workers and **177 USD** have been paid to upgrade the workers account.

## Automation and Management

In the outstanding worker operational costs for workers, you may have noticed that a fraction of the payouts (except for the steemfest worker) is asked for by the chainsquad account owned by [ChainSquad GmbH](http://chainsquad.com).  This fee covered the technical management of workers as well as developing automation for maintaining reoccurring tasks to facilitate escrow workers more efficiently over time. As these tools near completion, the fraction asked for in order to develop automation and development tools will drastically decrease.

## Review and Code Audits

Additionally to management tools, the code produced by freelancers needs to be reviewed by 3rd parties before funds can be released. This ensures that the produced code fits into the high quality standards of the existing code base.  It is our wish to be able to hand over the work of auditing code to more and more entities (companies and individual high-profile developers) to grow the knowledge of the underlying technology. Hence, if you have a profile of providing excellent code review and have experience in the Graphene library, you may want to contact the [BitShares Blockchain Foundation](http://www.bitshares.foundation).

# Final Words

In the future you can expect regular updates on the accounting of BitShares Blockchain Foundation to ensure the highest standards in transparency and accountability. We feel the deep desire to support the BitShares community and ensure that uncertainties that appear are covered and resolved as quickly as possible.

Further, we hope that we can continue to grow our reputation within the BitShares shareholders and the whole community to receive sufficient trust to do what we are planning to do with BitShares.

If you want to support our efforts, please don't hesitate to get in contact with us (`info@bitshares.foundation`) or donate to `donations.bitshares.foundation`. We would like to emphasise that the BitShares Blockchain Foundation is a registered **non-profit** entity in the Netherlands which means that all funds donated will need to go into following our foundations' goals: Growing BitShares. 

