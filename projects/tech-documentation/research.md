# Bitcoin Full Node Documentation

## Introduction

__What is a node?__  

A node is a computer that is running the Bitcoin program. 
More importantly, it is connected to other computers (running the same program) to create a network.

__What is the Bitcoin Network?__  

The Bitcoin Network is made up of everyone running the bitcoin software, better known as _bitcoin clients_.

__What does the network do?__  

People (well, bitcoin clients) on the network talk to each other. 
They pass on information about what’s going on in other parts of the network. 
This is done by sending each other messages. For example, 
a message could be information about a new _transaction_.

This sharing of information is what allows to everyone on the network to keep up-to-date, 
which is pretty important if you want to run a digital currency on the Internet.

The Bitcoin Network is described as a __“peer-to-peer network”__ because:

- everyone is connected to each other, so it’s a network.
- everyone on the network is equal, so we are peers.

## What is a full node?  

A full node is a program that fully validates transactions and blocks. 
Almost all full nodes also help the network by accepting transactions and blocks from other full nodes, 
validating those transactions and blocks, and then relaying them to further full nodes.   

Most full nodes also serve lightweight clients by allowing them to transmit their transactions to the network 
and by notifying them when a transaction affects their wallet. If not enough nodes perform this function, 
clients won’t be able to connect through the peer-to-peer network—they’ll have to use centralized services instead.

## Minimum Requirements  

Bitcoin Core full nodes have certain requirements. If you try running a node on weak hardware, 
it may work but you’ll likely spend more time dealing with issues. 
If you can meet the following requirements, you’ll have an easy-to-use node.

- Desktop or laptop hardware running recent versions of Windows, Mac OS X, or Linux

- 350 GB of free disk space, accessible at a minimum read/write speed of 100 MB/s

- 2 GB of memory (RAM)

- A broadband Internet connection with upload speeds of at least 400 kB (50 kB) per second.

- An unmetered connection, a connection with high upload limits, or a connection you regularly monitor to ensure it doesn’t exceed its upload limits. It’s common for full nodes on high-speed connections to use 200 GB upload or more a month. Download usage is around 20 GB/month, 
plus around an additional 340 GB the first time you start your node

- 6 hours/day that your full node can be left running. More hours would be better, and best of all would be if you can run your node continuously.(_tip_: disable "speed" or "suspend" options on screensaver for uninterrupted network traffic)

- Allow inbound connections to Bitcoin port 8333

## Possible Issues  

#### Legal  
Bitcoin use is prohibited or restricted in some areas.

#### Bandwidth limits  
Some Internet plans will charge an additional amount for any excess upload bandwidth used that isn’t included in the plan. 
Worse, some providers may terminate your connection without warning because of overuse. 
We advise that you check whether your Internet connection is subjected to such limitations 
and monitor your bandwidth use so that you can stop Bitcoin Core before you reach your upload limit.

#### Anti-virus  
Several people have placed parts of known computer viruses in the Bitcoin block chain. 
This block chain data can’t infect your computer, but some anti-virus programs quarantine the data anyway, 
making it more difficult to run Bitcoin Core. This problem mostly affects computers running Windows.

#### Attack target  
Bitcoin Core powers the Bitcoin peer-to-peer network, 
so people who want to disrupt the network may attack Bitcoin Core users in ways that will affect other things you do with your computer, 
such as an attack that limits your available download bandwidth.

## Download  
Bitcoin Core initial synchronization will take time and download a lot of data. 
You should make sure that you have enough bandwidth and storage for the full block chain size (over 350GB). 

**https://bitcoin.org/en/download**

## License  
Bitcoin Core is a community-driven free software project, released under the **MIT license**.

## Sources  

- Documentation for Bitcoin Core users and developers. https://en.bitcoin.it/wiki/Category:Bitcoin_Core_documentation
- Bitcoin Core. https://en.bitcoin.it/wiki/Bitcoin_Core
- Full node. https://en.bitcoin.it/wiki/Full_node
- Running Bitcoin. https://en.bitcoin.it/wiki/Running_Bitcoin
- Running A Full Node. https://bitcoin.org/en/full-node 
- Bitcoin.org Developer Documentation (GitHub). https://github.com/bitcoin-dot-org/developer.bitcoin.org
- Bitcoin network. https://en.wikipedia.org/wiki/Bitcoin_network
- Learn me a bitcoin. https://learnmeabitcoin.com/beginners/getting-started
