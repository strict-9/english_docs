# How to Mine $TTT-test on TrustNote2 Testnet Alpha Release

You’ve heard [TrustNote](https://trustnote.org/), the minable Public DAG ledger, and you’re ready to get your hands dirty on some of the latest crypto-currencies such as [$TTT](https://coinmarketcap.com/currencies/trustnote/). You can buy and trade $TTT, or you can “mine” for them. Mining $TTT on TrustNote is actually the process of a fair and trustable witness node selection for which the users are rewarded. This tutorial tells you how to mine TTT Test Notes on TrustNote 2.0 Alpha release using the basic tools on a PC running Ubuntu 18.0.4.

## Requirements
**Ubuntu 18.0.4**
This guide assumes that you are using Ubuntu 18.0.4. Before you begin, you should have a non-root user account with sudo privileges set up on your system.

**Node.js 8**
You can run node -v to check if you have installed Node.js 8 correctly. If not, you can check nodejs.org for how to install Node.js 8 on Ubuntu based Linux distributions.

**SQLite Version 3**
You can check this [tutorial](https://linuxhint.com/install-sqlite-ubuntu-linux-mint/) for how to install SQLite 3 on Ubuntu.

## Setup Your Super Node
Clone from the source:
```
git clone https://github.com/trustnote/trustnote-pow-supernode.git
```

Install the code using npm:
```
cd trustnote-pow-supernode
npm install
```

Start the mining service on your super node and wait for data synchronization to complete:
```
node start.js
```
Press Enter to accept the default actions when you are prompt for input.

The first time when the mining service is started, all data will be synchronized to your super node locally. It could take at least 12 hours to complete depending on your internet connection.

## Check Super Node’s Data Synchronization Status
Open a new terminal and connecting to the database:

```
sqlite3 ~/.config/trustnote-pow-supernode/trustnote.sqlite
```

Check how many rounds of data are synchronized by entering the following SQLite command from time to time:

```
sqlite>select max(round_index) from round;
```

You can compare this number with the number of current consensus round from the TrustNote2 [testnet explorer](http://explorer2-alpha.trustnote.org:8000/) and figure out how long it may take to synchronizthe rest of the data. It could take at least 12 hours to complete depending on your internet connection.

Note: it may take a few minutes before the number of current consensus round showing up on the web page after the testnet explorer is opened.

Whilst waiting, you can check your super node’s wallet address by entering the following SQLite command:

```
sqlite> select address from my_addresses;
```

## How to Get TTT Test Notes
To start with mine TTT Test Notes, you will need to have some TTT Test Notes to pay for your transactions on the TrustNote 2.0 testnet.

Email bob(at)trustnote.org with your super node’s wallet address and we will be glad to send you 10 MN (million notes) TTT Test Notes which is enough for you to start mining.

## Check My Mining Status
Once the rounds of data synchronized to your super node is the same as the number of current consensus round, you will see messages like below.

<p align="center">
  <img src="mining1.PNG">
</p>

Congratulations, you are starting to mine TTT Test Notes now!

## Check How Many TTT Test Notes I Have Mined
To check how many TTT Test Notes you have mined, open the TrustNote2 [testnet explorer](http://explorer2-alpha.trustnote.org:8000/), enter your Super Node’s wallet address in the search field and press the search button, you will see the changes of your wallet balance in line with the coinbase rewards you received and the transaction costs you have spent.

The message below shows the Coinbase rewards your super nodes receive during the mining process.

<p align="center">
  <img src="mining2.PNG">
</p>

## What’s Next?
Congratulations for your success on mining TTT Test Notes! I hope you enjoy it as much as I do! In the coming weeks, we’ll release more tools and tutorials, any comments and questions are welcomed!

Note this is just the very first release in our renewed TrustNote 2.0 [roadmap](https://github.com/TrustNoteDocs/community-committee/blob/master/ROADMAP.md), it is far from completion or perfection. To make it better, we welcome community members join us to test, develop, and discuss new features as we moving forward.

From time to time, as a community, we will evaluate the contributions made by every contributors. Volunteers that have provided significant contribution will be recognized for their outstanding work, and will be rewarded with $TTT tokens as appreciation (not payment) for the quality of the work submitted. Please reach me on bob(at)trustnote.org if you want to help.

Thanks for reading this. If you have any questions, please feel free to comment below or contacting me by email.
