---
language: en
layout: worker
type: escrow
bfid: 201808-trusty-community-ui-p1
workerid: not created yet
title: BitShares Community Wallet (Part 1/2)
name: Milos Preocanin
company:
 name: "AP Asia Tech Co., LTD. (Legal DAO representative of Trusty team)"
 url: "http://apasia.tech"
status:
discussions:
 - name: bitsharestalk
   url: "https://bitsharestalk.org/index.php?topic=26873.0"
price: 155000 USD
duration: 3 months
start: 2018/08/30
end: 2018/12/01
---

# **Who is Trusty (Introduction)**

We are Trusty team, business/product/technology specialists, willing to facilitate adoption of
BitShares blockchain by creating a bleeding edge app. Our passion is to offer to public a decentralized
exchange/wallet with top-notch UI/UX available across all mobile and web platforms. After research
we discovered that BitShares today is literally the only decentralized platform allowing such a bleeding
edge app to be developed and scaled globally. Existing 3rd party solutions, even native DEX UI doesn’t
unlock full potential of BitShares Blockchain (still with on-going development).

Another crucial reason we have chosen BitShares to be our blockchain-homeland is its incredible
community building up since 2014 (BitShares enjoys first mover advantage in the segment of
decentralized exchanges). Therefore, to prove our good will and integrity, we introduced ourselves by
contributing an open-source web framework for BitShares based on Vue . The web framework has
been tailored for BitShares to utilize it’s API calls and provide an intuitive SDK to create any kind of
decentralized applications on top of BitShares much easier and faster, than utilizing existing UI.

As a result we got a very positive feedback from the Community, especially from Milos and APAsia.tech team
leading to a very productive collaboration. Following our meeting in Thailand, we decided to unite our efforts 
for the growth and success of the BitShares eco-system. 
This worker is our first public step forward and APAsia.tech serves as our legal representative.

# **Vision**

Drive BitShares Community Wallet to become a trustless-solution for both novice and experienced
crypto users to conveniently hold, trade and manage any types of crypto assets and accessible from
any mobile or web platform. 

# **Worker Intent**

We intend to release final version of BitShares Community Wallet in 6 months. Due to strong total amount of the worker, 
worker is split to 2 smaller instances of it (3 months each). This allows the BitShares community to engage in an active review 
process after the first three months with the setup of the subsequent worker. The hourly rates for the subsequent worker will 
remain as is in this worker.

The main purpose of this proposal is to provide the Community  

**a User-Friendly, Trader-Oriented and fully responsive wallet.** 

This includes all common user settings, account management and the entire dex with trading, margins and deposit/withdraw (subject to cooperation of gateways).
The source will be MIT licensed, releases with web deployable and locally installable versions (via Electron) will be provided when feasible.

Launch of effective development process requires
- Defining a collaboration framework between Trusty team (Contractor) and BitShares DAC
(client)
- Providing a transparent mechanism to regularly deliver results to the client
- Establishing a budget to sustain development

Furthermore we seek to 
- Support [current UI team](https://www.bitshares.foundation/workers/2018-07-infrastructure) by enabling them to focus more on business development for DEX
and providing full API functionality, while Community has a working product to be used
- **not** replace of the [reference UI](https://github.com/bitshares/bitshares-ui)


## **Collaboration Framework**

We are using Git-based management system to ensure full transparency and accountability of the
project development. Below is the simple sequence of actions Trusty team will perform to deliver vest
results:

- List and continuously update development tasks on git, including tags of current status,
priority and sprint deadline
- Maintain timely communications with community members, posting issues or comments on
Git
- Favor feature usability (bugs fixing) over schedule and deliver the highest priority work first
- Deliver results for public beta testing by the end of every 3rd week (3 weeks sprints)
- Provide monthly reports of results against hours and costs of development
- Keep hours logged with TopTracker for entire team with reporting

## **Development Process**

We favor agile development process when all the workstreams (user journey, mockups, prototyping,
development, testing, documentation) are pushed simultaneously to release the highest priority
feature for public beta testing. Lean and interactive product development encourages faster user
feedback and ensures every new feature actually contributes to app usability. While designing trading
UI we will be using best market practice examples, Bitfinex and Huobi interfaces in particular.

## **Budget**

### **Team Positions and Rates**

| Roles (described below)             | Rate (bitUSD/h) |
| ---------------------------------- | -------------:|
| General Manager (Milos Preocanin)   |   $100.00     |
| Product Manager / UI/UX Liaison (Armen Azatyan)  |   $140.00     |
| QA and Testing      |    $80.00     |
| JS And Code review (Anton Lopan)      |	 $140.00     |
| Lead Front-End Developer / Architect, Code Review (Roman Sabirov)	 |    $80.00     |
| Full-stack Developer (Roman Bellendir)	         |    $80.00     |
| HTML and CSS Developer	         |    $50.00     |
| Front-End JS Developer             |	  $50.00     |
| Designer                           |	  $50.00     |

### **Initial Development Plan Part 1**

|                                    | Design | Lib*  | Markup* | UI/UX | Testing | Bug fixes | **Total** |
| ---------------------------------- |:------:|:-----:|:-------:|:-----:|:-------:|:---------:|----------:|
| Base Layouts                       |        | 0     | 80      |       |         |           |    **80** |
| Base architecture                  |        | 65    | 0       |       |         |           |    **65** |
| Account Management                 |   15   | 75    | 80      | 25    | 55      | 40        |   **290** | 
| Markets and place orders           |   30   | 125   | 100     | 50    | 110     | 70        |   **485** |
| Recent Tx/open orders              |    5   |  40   |  42     | 20    | 35      | 25        |   **167** |
| Deposit                            |   10   |  95   |  75     | 40    | 70      | 50        |   **340** |
| Withdrawal                         |   10   |  95   |  75     | 40    | 70      | 50        |   **340** |
| Infrastucture	                     |   10   |  65   |   0     | 20    | 35      | 25        |   **155** |
|    	                             |        |       |         |       |         |           |           |
| **TOTAL**	                         |        |       |         |       |         |           |  **1922** |

*Total represent maximum amount of working hours for the budget of this Worker

*10000 USD is included fixed fee for the escrow partner, for the duration of 3 months in total. 

## **Team Bios**

### Milos Preocanin
**Worker/Technology Manager**

Born in Serbia, with having a new home for last half decade in SE Asia, became a master of Linux
networking and administration before reaching his 20’s. Spent early days in ISP industry, where later
on moved to corporate IT management positions around foreign sectors in Serbia.
Track record in recent years of extensive web, app and hosting projects, now fusing long-term skills
with an extensive knowledge and ability to consult on all matters blockchain and cryptocurrency.
Today specializes in community management, turning ideas into reality, and enabling people to take
clear actions for project or business success.

Will ensure that there is proof of work delivered/time used against invoiced hours to the blockchain.
Also will be one and only point of PR for this worker, unless professional discussion between
developers is requested/needed.

### Armen Azatyan
**Business and Product Development**

5 years in IT entrepreneurship, 7 years in Investment banking. Ex. Social marketing director in
OnetwoTrip online travel agency, founder IFAB.ru, Trendever.com. Ex. Deutsche Bank, VTB Capital, 18
closed deals ECM and M&A (>$18bn in total).

Expert in business administration and customer experience. Will manage team and make sure that
BitShares DAC (Decentralized Exchange) meets the the top-notch app usability standards.

### Anton Lopan
**JS dev, Devops, Code review**

8 years in web development, from php5 heavy templates websites to serverless PWA (2 year of vuejs
currently). Really love to code, that’s why can do it even on Brainfuck or Haskell.
Got strong knowledge of current bitshares-ui, bitsharesjs, bitsharesjs-ws libs. Created first version of
trusty.fund upon bitshares-ui fork, then decided to rewrite from scratch using vue.
Specialist in Golang, JS, Bash.

Will provide best ways to build fast / scalable UI. Including integration of new features, code review
and pull request communication, full cover of CI / Devops processes, unit tests, bug fixes and technical
issues communication, propose bitshares-core features.

### Roman Sabirov
**Lead Front-End Developer, Architect, Code Review**

Development Experience: 5+ years of commercial front-end development which includes 3 years of
building complex web applications using Vue.js/Vuex and modern JS stack (es6+, babel, webpack,
scss). Lead Front-end developer of Trusty.Fund wallet application.

Will make architectural decisions, perform PR code reviews and develop main components of the
application.

### Roman Bellendir
**Fullstack Dev**

5 years in commercial web-development. 2 years was engaged in simulation of industrial production.
3 years was focusing on Android development. 1 year development of blockchain related products.
Working on backend and frontend services of Trusty, creating faucet, money sender service, android
app.

Specialist in NodeJs, Vue.js, Kotlin.

### Alex Volkov
**Web Designer**

Experience more than 3 years. Pro-user of photoshop and illustrator. Specialist in creating sites,
applications and printing. Focuses on designing of responsive interfaces. 

<hr>

# **Trusty's Open Source contribution and existing project**

Trusty's GitHub organization is  
 - https://github.com/TrustyFund
 
The above-mentioned Vuex wrapper for BitShares is already published an can be found here
 - https://github.com/TrustyFund/vuex-bitshares

Furthermore, a Portfolio Management App for Mobile has been developed, which is already live 
 - https://trusty.fund

**NOTICE/ADVERTISEMENT:**

Three more positions will be hired* and initially offered to the Developers around BitShares ecosystem:
1. Project Coordinator / Coordination, QA and Testing
2. HTML and CSS developer
3. Frontend JS developer

*For submissions please contact Milos by Telegram (@murda_ra), or in the discussion thread https://bitsharestalk.org/index.php?topic=26873.0 
