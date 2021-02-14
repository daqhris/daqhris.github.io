## What Is A Full Node?

A full node is a program that fully validates transactions and blocks. 
Almost all full nodes also help the network by accepting transactions and blocks from other full nodes, 
validating those transactions and blocks, and then relaying them to further full nodes.
Most full nodes also serve lightweight clients by allowing them to transmit their transactions to the network 
and by notifying them when a transaction affects their wallet. If not enough nodes perform this function, 
clients won’t be able to connect through the peer-to-peer network—they’ll have to use centralized services instead.

Many people and organizations volunteer to run full nodes using spare computing 
and bandwidth resources—but more volunteers are needed to allow Bitcoin to continue to grow. 
This document describes how you can help and what helping will cost you.


## Costs And Warnings
Running a Bitcoin full node comes with certain costs and can expose you to certain risks. 
This section will explain those costs and risks so you can decide whether you’re able to help the network.

### Special Cases
Miners, businesses, and privacy-conscious users rely on particular behavior from the full nodes they use, 
so they will often run their own full nodes and take special safety precautions. 
This document does not cover those precautions—it only describes running a full node to help support the Bitcoin network in general.

Please seek out assistance in the community 
if you need help setting up your full node correctly to handle high-value and privacy-sensitive tasks. 
Do your own diligence to ensure who you get help from is ethical, reputable and qualified to assist you.

### Secure Your Wallet
It’s possible and safe to run a full node to support the network and use its wallet to store your bitcoins, but you must take the same precautions you would when using any Bitcoin wallet. Please see the securing your wallet page for more information.

### Minimum Requirements
Bitcoin Core full nodes have certain requirements. If you try running a node on weak hardware, it may work—but you’ll likely spend more time dealing with issues. If you can meet the following requirements, you’ll have an easy-to-use node.

- Desktop or laptop hardware running recent versions of Windows, Mac OS X, or Linux.

- 350 gigabytes of free disk space, accessible at a minimum read/write speed of 100 MB/s.

- 2 gigabytes of memory (RAM)

- A broadband Internet connection with upload speeds of at least 400 kilobits (50 kilobytes) per second

- An unmetered connection, a connection with high upload limits, or a connection you regularly monitor to ensure it doesn’t exceed its upload limits. It’s common for full nodes on high-speed connections to use 200 gigabytes upload or more a month. Download usage is around 20 gigabytes a month, plus around an additional 340 gigabytes the first time you start your node.

- 6 hours a day that your full node can be left running. (You can do other things with your computer while running a full node.) More hours would be better, and best of all would be if you can run your node continuously.

#### Note: 
Many operating systems today (Windows, Mac, and Linux) enter a low-power mode after the screensaver activates, slowing or halting network traffic. 
This is often the default setting on laptops and on all Mac OS X laptops and desktops. 
Check your screensaver settings and disable automatic “sleep” or “suspend” options to ensure you support the network whenever your computer is running.

### Possible Problems
#### Legal: 
Bitcoin use is prohibited or restricted in some areas.

#### Bandwidth limits: 
Some Internet plans will charge an additional amount for any excess upload bandwidth used that isn’t included in the plan. 
Worse, some providers may terminate your connection without warning because of overuse. 
We advise that you check whether your Internet connection is subjected to such limitations 
and monitor your bandwidth use so that you can stop Bitcoin Core before you reach your upload limit.

#### Anti-virus: 
Several people have placed parts of known computer viruses in the Bitcoin block chain. 
This block chain data can’t infect your computer, but some anti-virus programs quarantine the data anyway, 
making it more difficult to run Bitcoin Core. This problem mostly affects computers running Windows.

#### Attack target: 
Bitcoin Core powers the Bitcoin peer-to-peer network, 
so people who want to disrupt the network may attack Bitcoin Core users in ways that will affect other things you do with your computer, 
such as an attack that limits your available download bandwidth.

## Download Bitcoin Core

Check your bandwidth and space
Bitcoin Core initial synchronization will take time and download a lot of data. 
You should make sure that you have enough bandwidth and storage for the full block chain size (over 350GB). 
If you have a good Internet connection, you can help strengthen the network by keeping your PC running with Bitcoin Core and port 8333 open. 
Read the full node guide for details.

Bitcoin Core is a community-driven free software project, released under the MIT license.

https://bitcoin.org/en/download

## Sources:
- Documentation for Bitcoin Core users and developers. https://en.bitcoin.it/wiki/Category:Bitcoin_Core_documentation
- Bitcoin Core. https://en.bitcoin.it/wiki/Bitcoin_Core
- Full node. https://en.bitcoin.it/wiki/Full_node
- Running Bitcoin. https://en.bitcoin.it/wiki/Running_Bitcoin
- Running A Full Node. https://bitcoin.org/en/full-node 
- Bitcoin.org Developer Documentation (GitHub). https://github.com/bitcoin-dot-org/developer.bitcoin.org
- Bitcoin network. https://en.wikipedia.org/wiki/Bitcoin_network