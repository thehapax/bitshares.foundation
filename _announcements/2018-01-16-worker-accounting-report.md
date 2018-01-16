---
title: Accounting Report 2018-01
---

# What is this report

This report serves as a financial report for the
`workers.bitshares.foundation` account which is owned by the BitShares
community and managed by the BitShares Blockchain Foundation (BBF) to
operate so called escrow-workers. These obtain BTS from the BitShares
DAC and pay freelancers in bitUSD according to the rules set forth in
their individial worker proposals.

# To whom is this report directed

The report is meant to inform all BTS holders and serve as a base for
transparency with respect to funds that are in control by the BBF as
a trustee.

# Report

## Reporting Period

The BBF started its work with creating the first worker proposal
`201707-bsip18` in 2017/07/12. Thus, 6 months have
passed.

## Statistics

We have produced 1065 transactions in our accounting affecting 54
accounts in our local books.

## Workers

The following workers have been created by the BBF

```
 * 201707-bsip18
 * 201708-bitsharesui
 * 201709-steemfest
 * 201710-compliance
 * 201710-spokesperson
 * 201712-blockchainacademy
 * 201712-infrastructure
 * 201801-budget-chinese-translations
```

Of which **6** workers have been approved by the BTS holders and receive
funds from the working budget (reserve fund) of the BitShares DAC.

This is the output of our accounting management interface:
```
vesting    worker    worker                              start       end         balance          claimable         asked             outstanding      nonescrow          escrow           progress
---------  --------  ----------------------------------  ----------  ----------  ---------------  ----------------  ----------------  ---------------  -----------------  ---------------  ----------
1.13.1661  1.14.56   201707-bsip18                       2017/07/15  2017/10/31  0.00000 BTS      0.00000 BTS       23000.00000 USD   0.00000 USD            0.00000 USD  0.00000 USD      100 %
1.13.1737  1.14.58   201708-bitsharesui                  2017/08/15  2018/02/15  33133.23039 BTS  17,499.99990 BTS  150000.00000 USD  52962.50000 USD  17,796.830000 USD  52962.50000 USD  100 %
1.13.1862  1.14.59   201709-steemfest                    2017/09/20  2017/10/20  0.00000 BTS      0.00000 BTS       6666.00000 USD    0.00000 USD            0.00000 USD  0.00000 USD      100 %
1.13.2114  1.14.60   201710-compliance                   2017/10/18  2018/12/31  0.00000 BTS      0.00000 BTS       50000.00000 USD   50000.00000 USD        0.00000 USD  0.00000 USD      0 %
1.13.2115  1.14.61   201710-spokesperson                 2017/10/18  2018/12/31  0.00000 BTS      5,625.00000 BTS   50000.00000 USD   50000.00000 USD        0.00000 USD  50000.00000 USD  100 %
1.13.2307  1.14.67   201712-infrastructure               2017/12/01  2018/05/31  0.00000 BTS      3,375.00000 BTS   19000.00000 USD   19000.00000 USD        0.00000 USD  19000.00000 USD  100 %
1.13.2325  1.14.68   201712-blockchainacademy            2017/12/01  2018/05/31  0.00000 BTS      0.00000 BTS       15000.00000 USD   15000.00000 USD        0.00000 USD  15000.00000 USD  100 %
1.13.2826  1.14.71   201801-budget-chinese-translations  2018/01/01  2018/06/30  0.00000 BTS      0.00000 BTS       6000.00000 USD    6000.00000 USD         0.00000 USD  0.00000 USD      0 %
```

## Working Budget / Reserve Fund

After the first 6 months, we have claimed **3,375,620.57896** BTS from
the reserves. Of these BTS have traded **2,760,007.45190** BTS into
**281,462.831800 USD**. We paid a total of **1,291.599688 USD**
equivalent in fees. The majority of the fees have been caused by
creating workers (~$88-$112 each) and claiming funds ($2-$22). Given
that the transaction fees have been reduced by the committee, we expect
operation costs to be reduced, significantly.

The approx. 3M BTS have been claimed through the following workers
accordingly:

```
  -600,799.76276 BTS    201707-bsip18
-2,091,833.32139 BTS    201708-bitsharesui
  -123,000.00000 BTS    201709-steemfest
  -384,375.00000 BTS    201710-spokesperson
   -81,562.49481 BTS    201712-blockchainacademy
   -94,050.00000 BTS    201712-infrastructure
====================
-3,375,620.57896 BTS
```

## Payouts

A total of 15 payouts to the following workers occured according to
their invoicing (see individual workers page):

 * [201708-bitsharesui](/worker/escrow/2017-08-bill-butler)
 * [201709-steemfest](/worker/escrow/2017-09-steemfest)
 * [201707-bsip18](/worker/escrow/2017-07-peter-conrad)
 * [201712-infrastructure](/worker/budget/2017-12-infrastructure)*

\* The infrastructure worker has only received BTS to maintain the
faucet account `onboarding.bitshares.foundation`.

## Currently in Escrow

As of the time of writing, a total of **141,962.500000 USD** lies in
escrow in the `bitshares.foundation` account which holds the funds for
these worker proposals:

```
   57,962.500000 USD      201708-bitsharesui:USD
   50,000.000000 USD      201710-spokesperson:USD
   15,000.000000 USD      201712-blockchainacademy:USD
   19,000.000000 USD      201712-infrastructure:USD
====================
  141,962.500000 USD
```

As such, all outstanding USD payouts for the currently registered and
approved workers under the BBF are **fully funded** in USD, today.
Additionally claimed BTS can be returned, directly.

## Workers account

The account `workers.bitshares.foundation` which is owned by the
BitShares community holds a total of 587,435.47426 BTS and 17,796.830000
USD.

Due to misconfigured automatic trading into BTS, an additional total of 
17,796.830000 USD are in the possession of this account that are
promised to be returned. As a consequence, the BBF will in the future
sell those USD back into BTS to properly send them to the reserve fund.
The automation has since been improved to avoid this inconvenience in
the future.

## "BurnFund"

A total of 576,078.66616 BTS is listed in the so called BurnFund which
describes the amount of BTS that will be returned to the reserve pool.

Our current strategy is to reserve those funds in medium-sized chunks to
avoid falsifying weekly statistics.

*Remark*: It is worth noting that the Foundation only subsidizes the
creation of the unapproved workers through the BurnFund which totals
1,820.95128 BTS.

# Donations

We would like to thank BitShares user @aloha for his generous donation
of 10,000 BTS which will be used to support ongoing operations of the
BBF. Further donors are: @zero-lemon, @lucid1980, and @chainsquad.
