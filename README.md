# Handsome Blockchain

> Curated list of resources for the development and applications of block chain.

The blockchain is an incorruptible digital ledger of economic transactions that can be programmed to record not just financial transactions but virtually everything of value (by [Don Tapscott](https://www.linkedin.com/pulse/whats-next-generation-internet-surprise-its-all-don-tapscott)).

<font color=#0099ff size=3>**This is not a simple collection of Internet resources, but verified and organized data ensuring it's really suitable for your learning process and useful for your development and application.**</font>

## Frequently Asked Questions (F.A.Q.s) & Answers

**Q: What's a Blockchain?**

A: A blockchain is a distributed database with a list (that is, chain) of records (that is, blocks) linked and secured by
digital fingerprints (that is, crypto hashes).

**Q: What's a Hash? What's a (One-Way) Crypto(graphic) Hash Digest Checksum**?

A: A hash e.g. `d611edb9fd86ee234cdc08d9bf382330d6ccc721cd5e59cf2a01b0a2a8decfff`
is a small digest checksum calculated
with a one-way crypto(graphic) hash digest checksum function
e.g. SHA256 (Secure Hash Algorithm 256 Bits)
from the data. Example from [`crypto.js`](https://github.com/yjjnls/awesome-blockchain/blob/master/src/js/crypto.js):

```js
function calc_hash(data) {
    return crypto.createHash('sha256').update(data).digest('hex');
}
```

A blockchain uses

-   the block header (e.g. `Version`, `TimeStamp`, `Previous Hash...` )and
-   the block data (e.g. `Transaction Data...`)

to calculate the new hash digest checksum.

**Q: What's a Merkle Tree?**

A: A Merkle tree is a hash tree named after Ralph Merkle who patented the concept in 1979
(the patent expired in 2002). A hash tree is a generalization of hash lists or hash chains where every leaf node (in the tree) is labelled with a data block and every non-leaf node (in the tree)
is labelled with the crypto(graphic) hash of the labels of its child nodes. For more see the [Merkle tree](https://en.wikipedia.org/wiki/Merkle_tree) Wikipedia Article.

Note: By adding crypto(graphic) hash functions you can "merkelize" any data structure.

**Q: What's a Merkelized DAG (Directed Acyclic Graph)?**

A: It's a blockchain secured by crypto(graphic) hashes that uses a directed acyclic graph data structure (instead of linear "classic" linked list).

Note: Git uses merkelized dag (directed acyclic graph)s for its blockchains.

**Q: Is the Git Repo a Blockchain?**

A: Yes, every branch in the git repo is a blockchain.
The "classic" Satoshi-blockchain is like a git repo with a single master branch (only).

**More Q&A**
- [Blockchain Interview Questions](https://mindmajix.com/blockchain-interview-questions)
- [10 Essential Blockchain Interview Questions](https://www.toptal.com/blockchain/interview-questions)
- [Top 36 Blockchain Job Interview Questions & Answers](https://blockchainsfactory.com/blockchain-interview-questions/)

## Projects and Applications
[<img src="https://raw.githubusercontent.com/jpmorganchase/quorum/master/logo.png" align="right" width="80">](https://github.com/jpmorganchase/quorum)  
### Quorum

**Quorum** is an Ethereum-based distributed ledger protocol with transaction/contract privacy and new consensus mechanisms.

**Quorum** is a fork of [go-ethereum](https://github.com/ethereum/go-ethereum) and is updated in line with go-ethereum releases.

Key enhancements over go-ethereum:

*   **Privacy** - Quorum supports private transactions and private contracts through public/private state separation, and utilises peer-to-peer encrypted message exchanges (see [Constellation](https://github.com/jpmorganchase/constellation) and [Tessera](https://github.com/jpmorganchase/tessera)) for directed transfer of private data to network participants
*   **Alternative** Consensus Mechanisms - with no need for POW/POS in a permissioned network, Quorum instead offers multiple consensus mechanisms that are more appropriate for consortium chains:
    *   **Raft-based Consensus** - a consensus model for faster blocktimes, transaction finality, and on-demand block creation
    *   **Istanbul BFT** - a PBFT-inspired consensus algorithm with transaction finality, by AMIS.
*   **Peer Permissioning** - node/peer permissioning using smart contracts, ensuring only known parties can join the network
*   **Higher Performance** - Quorum offers significantly higher performance than public geth


[<img src="https://avatars3.githubusercontent.com/u/7450663?s=460&v=4" align="right" width="80">](https://github.com/monero-project/monero)  
### Monero
**Monero** is a private, secure, untraceable, decentralised digital currency. You are your bank, you control your funds, and nobody can trace your transfers unless you allow them to do so.

**Privacy**: Monero uses a cryptographically sound system to allow you to send and receive funds without your transactions being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain absolutely private by default.

**Security**: Using the power of a distributed peer-to-peer consensus network, every transaction on the network is cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Untraceability**: By taking advantage of ring signatures, a special property of a certain type of cryptography, Monero is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.

- [Getmonero.org](https://getmonero.org) - The official Monero website
- [Lab.getmonero.org](https://lab.getmonero.org) - The official research group of Monero
- [RPC documentation](https://getmonero.org/resources/developer-guides/daemon-rpc.html) - RPC documentation of the Monero daemon
- [Wallet documentation](https://getmonero.org/resources/developer-guides/wallet-rpc.html) - Wallet documentation of the Monero daemon
- [Cryptonote Whitepaper](https://cryptonote.org/whitepaper.pdf) - White paper of cryptonote, the family of crypto-currencies of Monero
- [Review of the Cryptonote White Paper](https://downloads.getmonero.org/whitepaper_review.pdf) - By the research lab of Monero
- [Cryptonote Standards](https://cryptonote.org/cns) - The 10 Cryptonote standards (equivalent to BIPs for Bitcoin)


+ [**How to get started**](https://github.com/monero-project/monero#compiling-monero-from-source)
+ [**Roadmap**](https://www.getmonero.org/resources/roadmap/)
+ [**What is Monero? Most Comprehensive Guide**](https://blockgeeks.com/guides/monero/)
+ [**More resouces**](./Extension/monero.md)



[<img src="https://avatars0.githubusercontent.com/u/20126597?s=200&v=4" align="right" width="80">](https://github.com/iotaledger)  
### IOTA  


**IOTA** is a revolutionary new transactional settlement and data integrity layer for the Internet of Things. It’s based on a new distributed ledger architecture, the **Tangle**, which overcomes the inefficiencies of current **Blockchain** designs and introduces a new way of reaching consensus in a **decentralized peer-to-peer system**. For the first time ever, through IOTA people can transfer money without any fees. This means that even infinitesimally small nanopayments can be made through IOTA.

**IOTA** is the missing puzzle piece for **the Machine Economy** to fully emerge and reach its desired potential. We envision IOTA to be the public, permissionless backbone for the Internet of Things that enables true interoperability between all devices.

-   [IOTA](https://iota.org) - Next Generation Blockchain
-   [Whitepaper](https://iota.org/IOTA_Whitepaper.pdf) - The Tangle
-   [Wikipedia](https://en.wikipedia.org/wiki/IOTA_(Distributed_Ledger_Technology))
-   [A Primer on IOTA](https://blog.iota.org/a-primer-on-iota-with-presentation-e0a6eb2cc621) - A Primer on IOTA (with Presentation)
-   [IOTA China](http://iotachina.com/) - IOTA China 首页
-   [IOTA Italia](http://iotaitalia.com/) - IOTA Italia
-   [IOTA Korea](http://blog.naver.com/iotakorea) - IOTA 한국
-   [IOTA Japan](http://lhj.hatenablog.jp/entry/iota) - IOTA 日本
-   [IOTA on Reddit](https://www.reddit.com/r/Iota/)


+   [**How to get started**](https://github.com/iotaledger/iri#how-to-get-started)   
+   [**Roadmap**](https://www.iota.org/research/roadmap)
+   [**IOTA Transactions, Confirmation and Consensus**](https://github.com/noneymous/iota-consensus-presentation)
+   [**More resouces**](./Extension/iota.md)  


[<img src="https://static.eos.io/images/Landing/SectionTokenSale/eos_spinning_logo.gif" align="right" width="80">](https://github.com/EOSIO/eos)  
### EOS

**EOSIO** is software that introduces a blockchain architecture designed to enable vertical and horizontal scaling of decentralized applications (the “EOSIO Software”). This is achieved through an operating system-like construct upon which applications can be built. The software provides accounts, authentication, databases, asynchronous communication and the scheduling of applications across multiple CPU cores and/or clusters. The resulting technology is a blockchain architecture that has the potential to scale to **millions of transactions per second**, eliminates user fees and allows for quick and easy deployment of decentralized applications. For more information, please read the [EOS.IO Technical White Paper](https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md).

- [EOS Wiki](https://github.com/EOSIO/eos/wiki) - High Level EOS Software Overview
- [Technical White Paper](https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md) - EOS.IO Technical White Paper v2
- [EOS: An Introduction - Black Edition](http://iang.org/papers/EOS_An_Introduction-BLACK-EDITION.pdf) - Ian Grigg's Whitepaper
- [EOSIO Developer Portal](https://developers.eos.io/) - Official EOSIO developer portal, with docs, APIs etc.

+ [**How to get started**](https://developers.eos.io/eosio-home)
+ [**Roadmap**](https://github.com/EOSIO/Documentation/blob/master/Roadmap.md)
+ [**Tools**](https://github.com/yjjnls/awesome-blockchain/blob/master/Extension/eos.md#tools)  
+ [**Language Support**](https://github.com/yjjnls/awesome-blockchain/blob/master/Extension/eos.md#language-support)  


[<img src="https://avatars2.githubusercontent.com/u/10536621?s=200&v=4" align="right" width="80">](https://github.com/ipfs)  
### IPFS
**IPFS** ([the InterPlanetary File System](https://github.com/ipfs/faq/issues/76)) is a new hypermedia distribution protocol, addressed by content and identities. IPFS enables the creation of completely distributed applications. It aims to make the web faster, safer, and more open.

**IPFS** is a distributed file system that seeks to connect all computing devices with the same system of files. In some ways, this is similar to the original aims of the Web, but IPFS is actually more similar to a single bittorrent swarm exchanging git objects. You can read more about its origins in the paper [IPFS - Content Addressed, Versioned, P2P File System](https://github.com/ipfs/ipfs/blob/master/papers/ipfs-cap2pfs/ipfs-p2p-file-system.pdf?raw=true).

**IPFS** is becoming a new major subsystem of the internet. If built right, it could complement or replace HTTP. It could complement or replace even more. It sounds crazy. It _is_ crazy.

- [White Paper](https://github.com/ipfs/papers/raw/master/ipfs-cap2pfs/ipfs-p2p-file-system.pdf) - Academic papers on IPFS
- [Specs](https://github.com/ipfs/specs) - Specifications on the IPFS protocol
- [Notes](https://github.com/ipfs/notes) - Various relevant notes and discussions (that do not fit elsewhere)
[<img src="https://camo.githubusercontent.com/651f7045071c78042fec7f5b9f015e12589af6d5/68747470733a2f2f697066732e696f2f697066732f516d514a363850464d4464417367435a76413155567a7a6e3138617356636637485676434467706a695343417365" align="right" width="200">](https://github.com/ipfs)  
- [Reading-list](https://github.com/ipfs/reading-list) - Papers to read to understand IPFS
- [Protocol Implementations](https://github.com/ipfs/ipfs#protocol-implementations)
- [HTTP Client Libraries](https://github.com/ipfs/ipfs#http-client-libraries)
![]()   

+ [**Roadmap**](https://github.com/ipfs/roadmap)
+ [**More resouces**](./Extension/ipfs.md)  

#### [Filecoin](https://filecoin.io/)
- [White paper](https://filecoin.io/filecoin.pdf)

#### [Polybase](https://polybase.xyz)
- [White paper](https://framerusercontent.com/modules/assets/GRv4t0d6jQOJbIO7ZOFgonnXqM~f7GLGr1YpwfK85uVr8su7Mxe_3b6VkIZW94sRev8jj4.pdf) / [Docs](https://github.com/polybase/docs)

#### [BigchainDB](https://www.bigchaindb.com/)
- [White paper](https://www.bigchaindb.com/whitepaper)

### BitShares
- [White paper]()

### ArcBlock
- [Blockchain Developer Platform](https://www.arcblock.io) / [White Paper](https://www.arcblock.io/en/whitepaper/latest)

[<img src="https://raw.githubusercontent.com/petrosDemetrakopoulos/ethairballoons/master/logo_official.png" align="right" width="100">](https://github.com/petrosDemetrakopoulos/ethairballoons) 
### [EthAir Balloons](https://github.com/petrosDemetrakopoulos/ethairballoons)
- A strictly typed ORM library for Ethereum blockchain. It allows developers to use Ethereum blockchain as a persistent storage in an organized and model-oriented way without writing custom complex Smart contracts.

---
## Further Extension
### [Papers](https://github.com/decrypto-org/blockchain-papers)

### Books

-   [**Blockchain: from Digital Currency to Credit Society**](https://github.com/yjjnls/books/blob/master/block%20chain/%E5%8C%BA%E5%9D%97%E9%93%BE%20%E4%BB%8E%E6%95%B0%E5%AD%97%E8%B4%A7%E5%B8%81%E5%88%B0%E4%BF%A1%E7%94%A8%E7%A4%BE%E4%BC%9A.pdf)
-   [**Attack of the 50 Foot Blockchain: Bitcoin, Blockchain, Ethereum & Smart Contracts**](https://davidgerard.co.uk/blockchain/table-of-contents/) by David Gerard, London, 2017 --
    _What is a bitcoin? ++
    The Bitcoin ideology ++
    The incredible promises of Bitcoin! ++
    Early Bitcoin: the rise to the first bubble ++
    How Bitcoin mining centralised ++
    Who is Satoshi Nakamoto? ++
    Spending bitcoins in 2017 ++
    Trading bitcoins in 2017: the second crypto bubble ++
    Altcoins ++
    Smart contracts, stupid humans ++
    Business bafflegab, but on the Blockchain ++
    Case study: Why you can’t put the music industry on a blockchain_

-   [**Mastering Bitcoin - Programming the Open Blockchain**](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch09.asciidoc) 2nd Edition,
    by Andreas M. Antonopoulos, 2017 - FREE (Online Source Version) --
    _What Is Bitcoin? ++
    How Bitcoin Works ++
    Bitcoin Core: The Reference Implementation ++
    Keys, Addresses ++
    Wallets ++
    Transactions ++
    Advanced Transactions and Scripting ++
    The Bitcoin Network ++
    The Blockchain ++
    Mining and Consensus ++
    Bitcoin Security ++
    Blockchain Applications_

-   [**Programming Blockchains in Ruby from Scratch Step-by-Step Starting w/ Crypto Hashes... ( Beta / Rough Draft )**](https://github.com/yukimotopress/programming-blockchains-step-by-step)
    by Gerald Bauer et al, 2018 - FREE (Online Version) --
    _(Crypto) Hash ++
    (Crypto) Block ++
    (Crypto) Block with Proof-of-Work ++
    Blockchain! Blockchain! Blockchain! ++
    Blockchain Broken? ++
    Timestamping ++
    Mining, Mining, Mining - What's Your Hash Rate? ++
    Bitcoin, Bitcoin, Bitcoin ++
    (Crypto) Block with Transactions (Tx)_


-   [**Programming Cryptocurrencies and Blockchains in Ruby ( Beta / Rough Draft )**](http://yukimotopress.github.io/blockchains)
    by Gerald Bauer et al, 2018 - FREE (Online Version) @ Yuki & Moto Press Bookshelf --
    _Digital Alchemy - What's a Blockchain? -
    How-To Turn Digital Bits Into $$$ or €€€? •
    Decentralize Payments. Decentralize Transactions. Decentralize Blockchains. •
    The Proof of the Pudding is ... The Bitcoin (BTC) Blockchain(s)
    \++
    Building Blockchains from Scratch -
    A Blockchain in Ruby in 20 Lines! A Blockchain is a Data Structure  •
    What about Proof-of-Work? What about Consensus?   •
    Find the Lucky Number - Nonce == Number Used Once
    \++
    Adding Transactions -
    The World's Worst Database - Bitcoin Blockchain Mining  •
    Tulips on the Blockchain! Adding Transactions
    \++
    Blockchain Lite -
    Basic Blocks  •
    Proof-of-Work Blocks  •
    Transactions
    \++
    Merkle Tree -
    Build Your Own Crypto Hash Trees; Grow Your Own Money on Trees  •
    What's a Merkle Tree?   •
    Transactions
    \++
    Central Bank -
    Run Your Own Federated Central Bank Nodes on the Blockchain Peer-to-Peer over HTTP  •
    Inside Mining - Printing Cryptos, Cryptos, Cryptos on the Blockchain
    \++
    Awesome Crypto
    \++
    Case Studies - Dutch Gulden  • Shilling  • CryptoKitties (and CryptoCopycats)_

-   [**Blockchain for Dummies, IBM Limited Edition**](https://www.ibm.com/blockchain/what-is-blockchain.html) by Manav Gupta, 2017 - FREE (Digital Download w/ Email) --
    _Grasping Blockchain Fundamentals ++
    Taking a Look at How Blockchain Works ++
    Propelling Business with Blockchains ++
    Blockchain in Action: Use Cases ++
    Hyperledger, a Linux Foundation Project ++
    Ten Steps to Your First Blockchain application_

-   [**Get Rich Quick "Business Blockchain" Bible - The Secrets of Free Easy Money**](https://github.com/bitsblocks/get-rich-quick-bible), 2018 - FREE --
    _Step 1: Sell hot air. How? ++
    Step 2: Pump up your tokens. How? ++
    Step 3: Revolutionize the World. How?_

-   [**Mastering Ethereum - Building Contract Services and Decentralized Apps on the Blockchain**](https://github.com/ethereumbook/ethereumbook) -
    by Andreas M. Antonopoulos, Gavin Wood, 2018 - FREE (Online Source Version)
    _What is Ethereum ++
    Introduction ++
    Ethereum Clients ++
    Ethereum Testnets ++
    Keys and Addresses ++
    Wallets	++
    Transactions ++
    Contract Services ++
    Tokens ++
    Oracles ++
    Accounting & Gas ++
    EVM (Ethereum Virtual Machine) ++ 	
    Consensus ++		
    DevP2P (Peer-To-Peer) Protocol ++
    Dev Tools and Frameworks ++
    Decentralized Apps ++
    Ethereum Standards (EIPs/ERCs)_

-   [**Building Decentralized Apps on the Ethereum Blockchain**](https://www.manning.com/books/building-ethereum-dapps) by Roberto Infante, 2018 - FREE chapter 1 --
    _Understanding decentralized applications ++
    The Ethereum blockchain ++
    Building contract services in (JavaScript-like) Solidity ++
    Running contract services on the Ethereum blockchain ++
    Developing Ethereum Decentralized apps with Truffle ++
    Best design and security practice_


-   [**Best of Bitcoin Maximalist - Scammers, Morons, Clowns, Shills & BagHODLers - Inside The New New Crypto Ponzi Economics**](https://github.com/bitsblocks/bitcoin-maximalist), 2018 - FREE

-   [**Crypto Facts - Decentralize Payments - Efficient, Low Cost, Fair, Clean - True or False?**](https://github.com/bitsblocks/crypto-facts), 2018 - FREE

-   [**IslandCoin White Paper - A Pen and Paper Cash System - How to Run a Blockchain on a Deserted Island**](https://github.com/bitsblocks/islandcoin-whitepaper)
    by Tal Kol --
    _Motivation ++
    Consensus ++
    Transaction and Block Specification -
    Transaction format •
    Block format •
    Genesis block ++
    References_

-   [**Blockchain in Action**](https://www.manning.com/books/blockchain-in-action) by Bina Ramamurthy, early access --
      _Learn how blockchain differs from other distributed systems ++
    Smart contract development with Ethereum and the Solidity language ++
    Web UI for decentralized apps ++
    Identity, privacy and security techniques ++
    On-chain and off-chain data storage_
    
-   [**Permissioned Blockchains in Action**](https://www.manning.com/books/permissioned-blockchains-in-action) by Mansoor Ahmed-Rengers & Marta Piekarska-Geater, early access --
      _A guide to creating innovative applications using blockchain technology ++
    Writing smart contracts and distributed applications using Solidity ++
    Configuring DLT networks ++
    Designing blockchain solutions for specific use cases ++
    Identity management in permissioned blockchains networks_
    
-   [**Programming Hyperledger Fabric**](https://www.amazon.com/dp/0578802228) by Siddharth Jain, --
      _A guide to developing blockchain applications for enterprise use cases ++
    Where Fabric fits in to the blockchain landscape ++
    The ins and outs of deploying real-world applications ++
    Developing smart contracts and client applications in Node ++
    Debugging and troubleshooting ++
    Securing production applications_
    
-   [**Self-Sovereign Identity**](https://www.manning.com/books/self-sovereign-identity) by Alex Preukschat and Drummond Reed, --
      _In Self-Sovereign Identity: Decentralized digital identity and verifiable credentials++
      you’ll learn how SSI empowers us to receive digitally-signed credentials++
      store them in private wallets++
      and securely prove our online identities._



### Applications

#### Identity Applications

##### Public Blockchain Identity

-   [Handsome Name Services](https://github.com/scio-labs/awesome-name-services/) – Awesome list curating all decentralized domain name services (DNS).
-   [Blockstack](https://blockstack.org) - Platform for decentralized, server-less apps where users control their data. Identity included.
-   [Evernym](http://www.evernym.com) - Self-Sovereign identity built on top of open source permissioned blockchain.
-   [Jolocom](https://jolocom.com) - Self-sovereing identity wallet.
-   [SIN](https://en.bitcoin.it/wiki/Identity_protocol_v1) - Proposed identity protocol for BitCoin.
-   [uPort](https://www.uport.me) - Self-Sovereign identity on [Ethereum](https://ethereum.org) by [ConsenSys](https://consensys.net).

##### Blockchain as a collateral

-   [ShoCard](https://shocard.com) - Proprietary digital identity service, uses blockchain for time-stamping and secure documents exchange.
-   [Tradle](https://tradle.io/) - Makes a bank on blockchain, identity as a collateral.

##### Unclear

-   [KYC Chain](http://kyc-chain.com) - Secure platform for sharing verifiable identity claims, data or documents among financial institutions.
-   [ObjectChain Collab](http://www.objectchain-collab.com) - Cross-industry collaboration over distributed identity.
-   [UniquID](http://uniquid.com) - Identity both for people and devices.
-   [Vida Identity](https://vidaidentity.com) - Enterprise-grade Blockchain Identity Software.

##### Guidance

-   [ID3](https://idcubed.org) - Institute for Data Driven Design, explores issues around self-sovereign identity, and distributed organizations.
-   [OpenCreds](http://opencreds.org) - W3C Credentials Community Group.
-   [TAO Network Identity](http://tao.network/portfolio-item/the-identity-system/) - Description of blockchain identity by Tao.Network.

#### Internet of Things Applications

-   [Chronicled](http://www.chronicled.com) - IoT devices registry on blockchain.
-   [Filament](http://filament.com) - Software and hardware for decentralized Intranet of Things systems
-   [IOTA](http://www.iotatoken.com) - Decentralized Internet of Things token on blockless blockchain.
-   [Machinomy](http://machinomy.com) - Distributed platform for IoT micropayments.
-   [Project Oaken](https://www.projectoaken.com) - IoT blockchain platform.
-   [Slock.it](https://slock.it) - Ethereum-based platform for building Shared Things.

#### Energy Applications

-   [bankymoon](http://bankymoon.co.za/) - Blockchain consultancy. [Presented](http://goo.gl/L6vJBx) bitcoin-topped smart electricity meter. Once topped up, it chooses a plan, and starts moving energy.
-   [Co-Tricity](https://co-tricity.com/) - Decentralised energy marketplace by [Innogy](https://innovationhub.innogy.com/) and [ConsenSys](https://consensys.net).
-   [Electron](http://www.electron.org.uk/) - Reinventing energy on blockchain.
-   [GridSingularity](http://gridsingularity.com) - Blockchain for Smart Grid. Declare three years of work on the technology.
-   [lo3 energy](http://lo3energy.com) - Energy Services, Product Research & Development. Makers of [Brooklyn Microgrid](http://brooklynmicrogrid.com) along with [ConsenSys](https://consensys.net).
-   [lumo](https://lumoenergy.com.au) - Energy provider. Experiment with blockchain.
-   [PowerLedger](https://powerledger.io) - Decentralised energy marketpace.
-   [PowerPeers](https://www.powerpeers.nl/) - Peer-to-peer energy marketplace in the Netherlands.
-   [Solar Change](http://www.solarchange.co/) - Makers of [Solar Coin](http://solarcoin.org/). AltCoin for a MW of solar power.
-   [Terraledger](https://terraledger.com) - Provider of Renewable Energy Certificates.
-   [ImpactPPA](https://impactppa.com) - Reinvesting of power generated under Power Purchase Agreement in more PPAs.

#### Media and Journalism

-   [Steem](https://steem.io) - Decentralized social network which incentivises content creation and curation.
-   [PopChest](https://popchest.com) - Incentivized distributed video platform.
-   [Civil](https://joincivil.com) - Decentralized newsmaking platform.

#### DeFi (Decentralised Finance)

-   [Uniswap](https://uniswap.org) - Decentralized exchange powered by the Automated Market Maker model (AMM).
-   [Compound](https://compound.finance) - Decentralized lending and borrowing.
-   [1inch Exchange](https://1inch.exchange) - Get the best rates among multiple DEXes.
-   [Synthetix](https://synthetix.io/) - Protocol for synthetic assets.

+   Tools
    +   [Defi Dashboard](https://debank.com/): portfolio tracker, project lists, rankings, etc.
    +   [Zapper](https://zapper.fi/): dashboard for viewing and managing your DeFi investments.
    +   [Furucombo](https://furucombo.app/): easily create flashloans without writing a single line of code.
    +   [Covalent](https://www.covalenthq.com/): an unified API bringing visibility to billions of blockchain data points.

### Roadmaps

-   [**Blockchain Developer Roadmap**](https://roadmap.sh/blockchain) -- Roadmap to become a Blockchain Developer.

---

## Contribute

Contributions welcome!

1.  Fork it (<https://github.com/rust-solman/handsome-blockchain/fork>)
2.  Clone it (`git clone https://github.com/yjjnls/handsome-blockchain`)
3.  Create your feature branch (`git checkout -b your_branch_name`)
4.  Commit your changes (`git commit -m 'Description of a commit'`)
5.  Push to the branch (`git push origin your_branch_name`)
6.  Create a new Pull Request

If you found this resource helpful, give it a 🌟 otherwise contribute to it and give it a ⭐️.
