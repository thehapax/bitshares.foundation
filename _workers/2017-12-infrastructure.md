---
language: en
layout: worker
type: budget
bfid: 201712-infrastructure
workerid: 1.14.67
title: Deploy and maintain independent BitShares infrastructure
name: Blockchain Projects BV
company:
 name: Blockchain Projects BV
 url: http://blockchainprojectsbv.com
status: paying
discussions:
 - name: bitsharestalk
   url: https://bitsharestalk.org/index.php/topic,25291.0.html
price: $19,000
duration: 6 months
start: 2017/12/01
end: 2018/05/31
redirect_from: 
 - /workers/2017-12-infrastructure
 - /worker/escrow/2017-12-infrastructure
reports:
 - name: 2017-12-11 Roadmap
   url: https://github.com/blockchainprojects/2017-12-infrastructure/blob/master/Roadmap_2017-12-infrastructure.pdf
 - name: 2018-01-15 Interim report
   url: https://github.com/blockchainprojects/2017-12-infrastructure/blob/master/Interim_report_1_2017-12-infrastructure.pdf
 - name: 2018-01-15 Final development report
   url: https://github.com/blockchainprojects/2017-12-infrastructure/blob/master/Final_development_report_2017-12-infrastructure.pdf
payments:
 - date: 2018/02/16
   oid: 1.11.24473034
   amount: 7,615.65 bitUSD
invoices:
 - 201712-infrastructure/20180216-BitSharesEurope Faucet.pdf
 - 201712-infrastructure/20180216-Factuur 2018-4.pdf
 - 201712-infrastructure/20180216-Hetzner Invoice 20180203.pdf
 - 201712-infrastructure/20180216-Linode + AWS.PDF

---

# Worker Proposal

Given the growth of the BitShares ecosystem, we, [Blockchain Projects
BV](http://blockchainprojectsbv.com) feel that the network should become
more redundant and reduce its reliance on business partners that are
currently running nodes primarily. That said, we would like to deploy
independent servers and maintain the basic needs for a healthy BitShares
network, including, but not limited to, a faucet, public API nodes, and
seed nodes.

## BitShares Funded Faucet

We propose to run an independent faucet that 

* will be used by the reference web/light client,
* has a registrar account that is owned by the BitShares community (e.g. committee),
* redirects referral rewards to an account owned by all BitShares holders

That said, we would like to reuse the available infrastructure of the
**BitShares Blockchain Foundation** to get up and running quickly.

Thus, we would like to propose that the **registrar** account
`onboarding.bitshares.foundation` is owned by the `committee-account`.
The BitShares blockchain foundation has agreed to allow Blockchain
Projects BV to operated the `onboarding.bitshares.foundation` on trust.

The referral percentage for affiliates will be **70%**. This means that

* 30% of the referral rewards go to the onboarding account
* 70% of the reward go to the referrer, if no referrer is present, the
  registrar (onboarding account) will be used.

## Distributed Network of BitShares

The core component of this proposal is the distribution of the BitShares
network by means of deploying multiple nodes and offer public API
endpoints to improve latency, robustness and availability for the
BitShares ecosystem. Since this proposal is funded by the BitShares
ecosystem, we limit the use of the APIs to non-commercial activity.

### Distributed Network for Mainnet Nodes

With our orchestration tools, we would like to strengthen the BitShares
network by deploying more nodes.

These nodes offer 

* public API endpoints (*for non-commercial use*),
* seed nodes.

To anticipate the need for horizontal scaling, of the BitShares network,
a load-balancer is put in front of the new nodes, ideally with
geolocation-based round-robin/latency selection algorithms.

With the use of orchestration tools, we will be able to deploy on
different Cloud providers (docker cloud, EC2, Google Cloud, and others). 

### Automation of Docker Container Builds

Further, we would like to implement **automated builds** using docker
containers. These containers allow a very easy and fast deployment of
BitShares nodes. The automation docker cloud ensures that the public
sources of BitShares-core on Github are compiled in a transparent way,
additionally, the inclusion of further nodes will be greatly
facilitated. However, since the compilation is resource intensive, a
paid premium docker cloud package needs to be obtained.

### Distributed Network for Testnet Nodes

Additionally to the nodes provided for the BitShares **main net**, we
would like to implement the very same thing for the public testnet as
well. Initially, the most economic decision would be to reuse the
server infrastructure from the main net. Later (and especially during
stress testing), the testnet network should become more independent.

This will also allow us
to organize a much bigger Stress-Testing Infrastructure.

# Milestones

1. integrate and deploy reference faucet
2. develop docker containers
3. develop orchestration tooling
4. develop loadbalancer
5. test deployment and loadbalanced nodes
6. public nodes with load balancer in the U.S. on separate servers for redundancy
7. support SSL encryption on the load balancers
8. deploy additional load balancer and 2 public API nodes in Asia
9. include testnet nodes on those machines

As time progresses, more nodes will be added in the most economical
manner.

# Payment

Additionally, since we would like to run a faucet that pays account
registration fees, we ask for liquid BTS to directly fund the faucet
account.

It follows an outline of the cost positions and its denomination:

* **USD (Fee):** One-time setup fee - **3,300 USD**
* **USD (Fee):** Additional maintenance fee - **1,650 USD/month**
* **USD (Expense):** Payment of the server costs (EC2, Google Cloud, ...) - starting at **100 USD/month/server**
* **USD (Expense):** Docker Hub subscription for Continuous Integration of BitShares-Core - starting at **15 USD/month**
* **USD (Expense):** Wildcard SSL certificate -- **800 USD**

Additional, we ask for additional funding in BTS:

* **BTS (Fee):** Operating the public reference faucet **330 USD/month**
* **BTS (Expense):** LTM upgrade fee for committee-owned registrar account: **1,500 BTS**
* **BTS (Expense):** Funding for the faucet - currently **1.21396 BTS/account**

As you can see, we distinguish between fees and expenses. Note that
while the fee is fixed for the whole duration of the worker proposal,
the expenses may change depending on network growth. Obviously, as the
BitShares network grows, we expect growth of share price which allows
this worker to obtain new servers to match bandwidth demands.

The BitShares Blockchain Foundation runs the escrow operations and earns
10% of the overall fees to cover their own expenses.

Of course, our escrow partner will **publish invoices immediately**.

# Cost Overview

Reaching the milestones requires us to obtain at 6 servers and ideally
another 4 nodes for docker. We expect to create at least 10,000 accounts
in the next 6 months. In total:

     +     $3,300
     +     $800
     +      1,500 BTS * 0.08 USD/BTS
     + 6 * $1,650
     + 6 * $100 * 6
     + 6 * $15 * 4
     +     1.21396 BTS * 10,000 * 0.08 USD/BTS
     ============================
     = $19051.168

Thus, **we are asking for $19,000** for the **next 6 months**, or
$3166.66/month and keep the option to add additional servers as we grow
and if economically useful.

# Key Performance Indicator (KPI)

* Availability and latency of load balanced public API servers
* Number of registered accounts
* Global usage of docker containers
* Total referral rewards through onboarding faucet

If after 6 months, the BTS holders consider this worker a success, we
intend to extend our efforts with another worker proposal to keep the
deployed infrastructure up and running.

# Remark

* This worker proposal highly depends on the availability of the
  **bitshares.org domain** and the approval of its use by the owner of
  the domain.

* Terms&Service of BlockchainProjects BV applies with the BitShares
  DAC being referred to as `Client`

### Edits:

* 2017/12/11: Added milestone for faucet deployment and integration
