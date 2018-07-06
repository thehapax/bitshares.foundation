---
language: en
layout: worker
type: budget
bfid: 201807-infrastructure
workerid: 1.14.108
title: "Renewal 1: Deploy and maintain independent BitShares infrastructure"
name: Blockchain Projects BV
company:
 name: Blockchain Projects BV
 url: http://blockchainprojectsbv.com
status: paying
discussions:
 - name: bitsharestalk
   url: "https://bitsharestalk.org/index.php?topic=26778.0"
price: 32,860 USD
price_division:
    fixed: 13,860 USD
    variable: 19,000 USD
duration: 7 months
start: 2018/07/01
end: 2019/01/31
reports:
payments:
invoices:

---

# **Worker Proposal**

Given the growth of the BitShares ecosystem, we ([Blockchain Projects BV](http://blockchainprojectsbv.com/)) have been providing a basic infrastructure with the just expired infrastructure worker (reports can be [found here](http://www.bitshares.foundation/workers/2017-12-infrastructure)). The community has been contributing as well and the number of nodes for the reference wallet has been increased greatly.

That said, we would like to continue to provide the nodes that have been deployed with the last worker as well as the faucet for the reference wallet.

## **BitShares Funded Faucet**

We propose to continue faucet operations identically to the previous worker proposal:

* default faucet used by the reference web/light client
* registrar account that is owned by the BitShares community (through committee account)
* referral rewards to fund account create only
* excessive funds to be returned to the working budget of the BitShares Blockchain

Thus, the **registrar** account onboarding.bitshares.foundation remains and is owned by the committee-account. The BitShares Blockchain Foundation has agreed to allow Blockchain Projects BV to operate the onboarding.bitshares.foundation on trust. The referral percentage for affiliates remains at **70%**. This means that

* 30% of the referral rewards go to the onboarding account
* 70% of the reward go to the referrer, if no referrer is present, the registrar (onboarding account) will be used.

We would like to remind everyone about time and ip-based restrictions that are put in place to prevent abuse of this community services. Commercial use of this faucet is discouraged.

## **Distributed Network of BitShares nodes**

The core component of this proposal is the distribution of the BitShares network by means of deploying multiple nodes and offer public API endpoints to improve latency, robustness and availability for the BitShares ecosystem. Since this proposal is funded by the BitShares ecosystem, we limit the use of the APIs to non-commercial activity.


Additionally we will deploy premium SSL certificates for all nodes to tighten security, this includes the current 4 domains and 4 additional ES domains.

### **Distributed Network for Mainnet Nodes**

The three deployed BitShares nodes 

	eu.nodes.bitshares.ws
	us.nodes.bitshares.ws
	sg.nodes.bitshares.ws

will be continuously operated within the description of the last worker and reports.

### **Distributed Network for Testnet Nodes**

The deployed BitShares testnet node

	testnet.nodes.bitshares.ws

will be continuously operated within the description of the last worker and reports. If necessary, additional testnet nodes will be deployed.

### **Public Uptime Tracking**

Next to the status page of the load balancers, we intend to either add the nodes above to an existing uptime logging service or deploy our own. This will greatly improve transparency to the BTS holders and voters to see uptime and availability.

### **Automation of Docker Container Builds**

The **automated builds** using docker containers will continue to be available and maintained. These containers allow a very easy and fast deployment of BitShares nodes. The automation docker cloud ensures that the public sources of BitShares-core on Github are compiled in a transparent way, additionally, the inclusion of further nodes will be greatly facilitated.

During the last worker proposal, we have also managed automated builds for the BitShares testnet as well as for release **tags** and **pull requests** of the entire repository.

## **Elasticsearch BitShares nodes for public use**

Advanced features of the reference wallet require full history and advanced searching capabilities to function smoothly, which requires publicly available nodes with Elasticsearch support. This worker aims to deploy a ES cluster that will be accessible through all deployed infrastructure nodes.

This will greatly simplify the workflow of developers and business administration for BitShares and enable easy access to statistical data processing and charting.

## **Testnet stress test**

The previous stress test needed to be ended without finding the limit of the backend nodes.
The bottleneck was production the stress (in terms of transactions per second). Despite having obtained significant throughput, a separated stress test should be initiated to raise the known limits further.

For this, we develop an automated deployment for a stress producing server, a real-time dashboard to monitor the stress test as well as develop algorithms to produce accurate results from data obtained during stress testing. We will explore possibilities to add this into an existing open source explorer 
or directly in the BitShares UI.

For the stress test additional testnet backend nodes will be deployed as required, we also want to get the BitShares community on-board (as desired) to deploy as many nodes and stress producing servers as possible within economical reason.

# **Milestones**

1. Maintain deployed infrastructure from previous worker
2. Deploy public uptime tracking
3. Switching to premium SSL certificates for all infrastructure nodes
4. Setup of ES databases, cluster configuration and feeding through bitshares-core
5. Development of automated deployment and execution of stress-testing
7. Development of proper frontend for monitoring stress testing
8. Manage, execute the stress test
9. Create in-depth stress test report

As time progresses, more nodes will be added in the most economical manner.

# **Payment**

Operating the nodes:

* **USD (Fee):** Maintenance fee - **1,650 USD/month**
* **USD (Expense):** Payment of the server costs (Hetzner, EC2, Google Cloud, …) - starting at **100 USD/month/server**
* **USD (Expense):** Cost for obtaining premium SSL certificates, estimated at **50 USD/domain**

Operating the faucet:

* **BTS (Fee):** Operating the public reference faucet **330 USD/month**

Stress testing:

* **USD (Expense)**: Frontend & Backend Development - estimated maximum of 64 hours (8 person days, **125 USD / h**) giving **8,000 USD**
* **USD (Expense)**: Managing, executing and reporting for the stress test - estimated maximum of 32 hours (4 person days, **125 USD / h**) giving **4,000 USD**
* **USD (Expense):** Payment of the server costs (Hetzner, EC2, Google Cloud, …) - starting at **100 USD/month/server**

As you can see, we distinguish between fees and expenses. Note that while the total fees are fixed (13,860 USD) for the whole duration of the worker proposal, the expenses (approx. 19,000 USD) may change depending on network growth, server availability and actual hours spent on a task. Obviously, as the BitShares network grows, we expect growth of share price which allows this worker to obtain new servers to match bandwidth demands.

The BitShares Blockchain Foundation runs the escrow operations and earns 10% of the overall fees to cover their own expenses. Of course, our escrow partner will **publish invoices immediately**.

# **Cost Overview**

The total costs are summarized again (marked with ~ where estimated expense)

         7 * 1,650 USD     (node maintenance fee)
     +     7 * 330 USD     (faucet fee)
     +      8 * 50 USD     (premium SSL)
     + 8 * 7 * 100 USD ~   (node server costs)
     +       8,000 USD ~   (stress test development)
     +       4,000 USD ~   (stress test operations)
     +    10 * 100 USD ~   (stress test server costs)
     ============================
     = 32,860 USD


Thus, we are asking for **32,860 USD** for the next 7 months and keep the option to add additional servers as we grow and if economically useful. Please note that this amount includes variable cost (expenses) for servers and actual hours and for those only actual expenses will be billed (this includes server expenses starting from 01.06.2018, but not the fees from that month).

# **Key Performance Indicator (KPI)**

The KPIs from the last worker still apply

* Availability and latency of load balanced public API servers
* Number of registered accounts
* Global usage of docker containers
* Total referral rewards through onboarding faucet

Additionally this worker has

* Availability of Elasticsearch access
* Managing and reporting of the stress test

If after 7 months, the BTS holders consider this worker a success, we intend to extend our efforts with another worker proposal to keep the deployed infrastructure up and running.

# **Remark**

* Terms & Conditions of Blockchain Projects BV apply with the BitShares DAC being referred to as Client
