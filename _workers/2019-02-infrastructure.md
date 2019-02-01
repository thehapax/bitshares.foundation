---
language: en
layout: worker
type: budget
bfid: 201902-infrastructure
workerid: 
title: "Renewal 2: Deploy and maintain independent BitShares infrastructure"
name: Blockchain Projects BV
company:
 name: Blockchain Projects BV
 url: http://blockchainprojectsbv.com
status: paying
discussions:
 - name: bitsharestalk
   url: ""
price: 203,750 CNY (30,000 USD)
price_division:
    fixed: 81,500 CNY
    variable: 122,250 CNY
duration: 12 months
start: 2019/02/01
end: 2020/01/31

---

# **Worker Proposal**

Given the growth of the BitShares ecosystem, we ([Blockchain Projects BV](http://blockchainprojectsbv.com/)) have been providing a basic infrastructure with the former and soon to expire infrastructure worker (reports can be [found here](http://www.bitshares.foundation/workers/2018-07-infrastructure)). The community has been contributing as well and the number of nodes for the reference wallet has been kept at a healthy amount.

That said, we would like to continue to provide the nodes that have been deployed with the last worker. The reference faucet has been moved to [its own worker](https://www.bitshares.foundation/workers/2019-02-reference-faucet).

## **Distributed Network of BitShares nodes**

The core component of this proposal is the distribution of the BitShares network by means of deploying multiple nodes and offer public API endpoints to improve latency, robustness and availability for the BitShares ecosystem. Since this proposal is funded by the BitShares ecosystem, we limit the use of the APIs to non-commercial activity.

### **Distributed Network for Mainnet Nodes**

The three deployed BitShares nodes

	eu.nodes.bitshares.ws
	us.nodes.bitshares.ws
	sg.nodes.bitshares.ws

will be continuously operated within the description of the last worker.

### **Distributed Network for Testnet Nodes**

The deployed BitShares testnet node

	testnet.nodes.bitshares.ws

will be continuously operated within the description of the last worker. If necessary, additional testnet nodes will be deployed.

### **Public Uptime Tracking and Statistics**

Next to the status page of the load balancers, we intend to either add the nodes above to an existing uptime logging service or deploy our own. This will greatly improve transparency to the BTS holders and voters to see uptime and availability. This was also one of the milestones of the previous worker and has been delayed. There is no additional fee included for this.

A preview is shown here: http://88.198.69.93:3000

![image](https://raw.githubusercontent.com/bitshares-foundation/bitshares.foundation/201902-infrastructure/_workers/2019-02-infrastructure-grafana-preview.png)

### **Maintenance of Automation of Docker Container Builds**

The **automated builds** using docker containers will continue to be available and maintained. These containers allow a very easy and fast deployment of BitShares nodes. The automation docker cloud ensures that the public sources of BitShares-core on Github are compiled in a transparent way, additionally, the inclusion of further nodes will be greatly facilitated.

During the last worker proposal, we have also managed automated builds for the BitShares testnet as well as for release **tags** and **pull requests** of the entire repository.

## **Elasticsearch BitShares nodes for public use**

Advanced features of the reference wallet require full history and advanced searching capabilities to function smoothly, which requires publicly available nodes with Elasticsearch support. This worker continues to provide a ES cluster that is accessible at

    https://elasticsearch.bitshares.ws (direct ES access, http authentification BitShares:Infrastructure)
    https://wrapper.elasticsearch.bitshares.ws (python wrapper)
    https://wrapper.elasticsearch.bitshares.ws/apidocs/ (python wrapper docs)

This will greatly simplify the workflow of developers and business administration for BitShares and enable easy access to statistical data processing and charting. Since the Elastic Search plugin from the bitshares-core is now stable, this will be used more extensively in the future.

# **Commercial use**
In the past there have been several instances of for-profit use of the services provided in this proposal. 
Any commerical usage of the nodes and elastic search endpoints included in this proposal will be recognized, and we 
will contact the offending party to either cease the usage or seek an agreement. The agreement can be simply a fee 
for the increased costs (which will directly flow into the budget of this worker) or provision of additional nodes through the offending party (decided case by case). This is nothing new, but will now be enforced more pro-actively.

# **Milestones**

1. Maintain deployed infrastructure 
2. Maintain ES cluster deployment
3. Maintain ES wrapper deployment
4. Monitoring and Statistics

As time progresses, more nodes will be added in the most economical manner.

# **Payment**

Operating the nodes:

* **USD (Fee):** Maintenance fee - **1,000 USD/month**
* **USD (Expense):** Payment of the server costs (Hetzner, EC2, Google Cloud, …) - starting at **100 USD/month/server**

As you can see, we distinguish between fees and expenses. Note that while the total fees are fixed (12,000 USD) for the whole duration of the worker proposal, the expenses (approx. 18,000 USD) may change depending on network growth, server availability and actual hours spent on a task, this includes expenses for server costs starting February 2019. Obviously, as the BitShares network grows, we expect growth of share price which allows this worker to obtain new servers to match bandwidth demands.

The BitShares Blockchain Foundation runs the escrow operations and earns 5% of the overall fees to cover their own expenses. Of course, our escrow partner will **publish invoices immediately**.

# **Cost Overview**

The total costs are summarized again (marked with ~ where estimated expense)

          12 * 1,000 USD     (node maintenance fee)
     + 12 * 10 * 150 USD ~   (node server costs)
     ===============================================
     =        30,000 USD     (203,750 CNY)


Thus, we are asking for **203,750 CNY** for the next 12 months and keep the option to add additional servers as we grow and if economically useful. Please note that this amount includes variable cost (expenses) for servers and actual hours and for those only actual expenses will be billed. We will also optimize existing server costs and switch hosters if necessary.

# **Key Performance Indicator (KPI)**

The following KPIs apply

* Availability and latency of load balanced public API servers
* Availability of Elasticsearch access
* Availability of Statistics overview (Grafana)

If after 12 months, the BTS holders consider this worker a success, we intend to extend our efforts with another worker proposal to keep the deployed infrastructure up and running.

# **Summary to the BTS holder**

This proposal maintains the reliable infrastructure we have built with previous infrastructure proposal, lowers the 
maintenance fees and includes statistics (preview here http://88.198.69.93:3000, traffic can be split up in origin as well 
allowing identifying for-profit use according to section **Distributed Network of BitShares nodes**). The elastic search 
included in this proposal is already in use be the reference UI for account history export and other BitShares Blockchain 
explorers.

# **Remark**
* The infrastructure and servers are up and running and produce costs. In the case that this proposal is not approved in time, the performance and connectivity of servers will be gradually reduced after a grace period.
* Terms & Conditions of Blockchain Projects BV apply with the BitShares DAC being referred to as Client
