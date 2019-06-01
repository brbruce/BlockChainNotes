# Blockchain Tech Dev Notes

---

## Links

Ethereum Whitepaper

<https://github.com/ethereum/wiki/wiki/White-Paper#applications>

Blockchain Train Blog

<http://decentralized.blog/catching-the-blockchain-train.html>

Safari - Blockchain for dummies

<https://www.safaribooksonline.com/library/view/blockchain-for-dummies/9781119365594/01_9781119365617-ffirs.xhtml>

Bitcoin

<https://bitcoin.org/en/developer-guide>

Ethereum

<https://github.com/ethereum/wiki/wiki/White-Paper>  
<https://media.consensys.net/the-state-of-the-ethereum-network-949332cb6895>  
<https://dappsforbeginners.wordpress.com/>

Truffle IDE Ethereum

<https://truffleframework.com/tutorials/ethereum-overview>

---

## Terms

Decentralized - Direct connection between users and providers. No third party.  
Peer to peer

Distributed

Byzantine fault tolerance - Not sure if failure has occurred or not, could also be lying.

Trustless

Consensus Process

Proof of work

Smart contract ecosystem

dApp - Distributed apps - (DAPP)

Hyperleger, Distributed ledger technology (DLT)

Decentralised Autonomous Organization (DAO)

Miners, Minters/Forgers

Oracles - Service which take external data and add as a transaction to be used in smart contracts. Centralized??? "An oracle pushes the data onto the blockchain rather than a smart contract pulling it in."

Solidity - Ethereum programming language for smart contracts.  
https://solidity.readthedocs.io/en/v0.4.24/

Gas?

Internal vs external functions?

---

### Consensus algorithms

https://hackernoon.com/a-hitchhikers-guide-to-consensus-algorithms-d81aae3eb0e3

In the world of crypto, consensus algorithms exist to prevent double spending.
Proof-of-work - Mining  
Proof-of-stake - Minting, Forging  
DPOS  
Proof-of-authority  
Proof-of-weight  
Byzantine Fault Tolerance

- PBFT - Centralized, permissioned
- Federated BFT - good one
- Directed Acyclic Graphs (DAGs) — aka the Blockchain Killers!

### Permissionless (Public) vs Permissioned (Federated) and Tokens

Only permissionless ledgers (public Blockchains like Bitcoin or Ethereum), need some sort of incentive mechanism to guarantee that block validators do their job according to the predefined rules.

In permissioned (federated/consortium/private) distributed ledger systems, validators and block-creators may be doing their job for different reasons: i.e., if they are contractually obligated to do so. In permissioned environments, validators can only be members of the club and are manually and centrally controlled.

**Permissioned ledgers, therefore, don’t need a token.** Also, please note that the term blockchain in the context of such ledgers is highly controversial.

### Tokens

https://blockchainhub.net/tokens/

- Intrinsic, Native or Built-in Tokens - of blockchains like Bitcoin, Ether, etc that serve as: (a) block validation incentives (‘miner rewards’); and (b) transaction spam prevention. The logic behind this is that if all transactions are paid, it limits the ability to spam.

- Application Tokens - With Ethereum, tokens can now easily be issued on the application layer through smart contracts on the Ethereum Blockchain as so-called complex dApp tokens or complex DAO tokens.

- Asset-backed tokens - that are issued by a party onto a blockchain for later redemption. They are the digital equivalent to physical assets. They are claims on an underlying asset (like the gold), that you need to claim from a specific issuer (the goldsmith). The transactions as tokens get passed between people are recorded on the blockchain. To claim the underlying asset, you send your token to the issuer, and the issuer sends you the underlying asset.

### Consensus mechanism: Proof-of-work vs Proof-of-stake

POW - Use CPU and electricity to calculate hash of the next block. Get a reward of 12.5 BTC/block + transaction fee. Difficulty increases to maintain constant time to solve.  
POS - Less electricity required. Next block assigned to user based on random or age-based, and size of user's stake. No reward, only transaction fee.

### Distributed Ledger Technology (DLT)

Distributed Ledgers are mostly known because of their use as cryptocurrencies, even if technically speaking the cryptocurrency and the underlying ledger are two different things.

However, in practice, a distributed ledger needs to have a cryptocurrency (proprietary or used from other ledger) in order to provide incentives to keep the nodes up and running.

For use as a distributed ledger, a blockchain is typically managed by a peer-to-peer network collectively adhering to a protocol for inter-node communication and validating new blocks. Once recorded, the data in any given block cannot be altered retroactively without alteration of all subsequent blocks, which requires consensus of the network majority.

Blockchains are secure by design and exemplify a distributed computing system with high Byzantine fault tolerance. Decentralized consensus has therefore been achieved with a blockchain.

### Directed Acyclic Graphs (DAG)

The meaning of the word "blockchain" remains controversial. While some people state it is synonymous with a Distributed Ledger (and most of generalist press tends to use it with this meaning), others argue that technically it would only apply to linear blockchains such as the one Bitcoin or Litecoin use and not to Directed Acyclic Graphs such as the ledgers based on Iota, Tangle, or Hedera Hashgraph algorithms. Therefore according to the latter definition, not all distributed ledgers have to necessarily employ a chain of blocks to successfully provide secure and valid achievement of distributed consensus: a blockchain is only one type of data structure considered to be a distributed ledger.

### Merkle Tree

Tree structure where leaf hashes are based on the data in the leaves, and non-leaf hashes are based on the hash of the concatenated leaf hashes.

### Patricia Tree (Radix Tree) - Ethereum accounts

### Nonce -

One-time use ids

### Hyperledger Fabric

Hyperledger Fabric is a permissioned blockchain infrastructure, originally contributed by IBM[19] and Digital Asset, providing a modular architecture with a delineation of roles between the nodes in the infrastructure, execution of Smart Contracts (called "chaincode" in Fabric) and configurable consensus and membership services.

A Fabric Network comprises "Peer nodes", which execute chaincode, access ledger data, endorse transactions and interface with applications. "Orderer nodes" which ensure the consistency of the blockchain and deliver the endorsed transactions to the peers of the network, and MSP services, generally implemented as a Certificate Authority, managing X.509 certificates which are used to authenticate member identity and roles.[20]

Fabric is primarily aimed at integration projects, in which a Distributed Ledger Technology (DLT) is required, offering no user facing services other than an SDK for Node.js, Java and Go.

### Tokens vs Cryptocurrencies

https://masterthecrypto.com/differences-between-cryptocurrency-coins-and-tokens/

altcoins are separate currencies with their own separate blockchain while tokens operate on top of a blockchain that facilitates the creation of decentralized applications.

### Privacy

https://masterthecrypto.com/privacy-coins-anonymous-cryptocurrencies/

Not always private

Privacy: The amount of coins you own, send and receive are not observable, traceable nor linkable by way of transaction history on the Blockchain

Fungibility: Every coin is worth the same value and is thus mutually interchangeable. No coin risks potential blacklisting nor debasement due to deprecating transaction history.

Decentralization: All nodes have equal power and control; there are no nodes that have more influence than others, i.e. masternodes. The currency is not created, maintained nor represented by any one person or company, i.e. a central authority.

Crypto currencies:
Monero - Very private
Bitcoin - Not private. Transparent, easy to trace.

### Wallets

https://masterthecrypto.com/guide-to-cryptocurrency-wallets/

### UTXO (bitcoin) vs Accounts (Ethereum)

https://ethereumbuilders.gitbooks.io/guide/content/en/design_rationale.html

---

## Components

Distributed File System

- Sia, Swarm, Storj

Distributed Web

- IPFS - Interplanetary File System
  - Uses distributed hash table - Used for DNS, multicast, instant messaging, bittorrent.
- Distributed Caching - https://en.wikipedia.org/wiki/Distributed_hash_table
  - Consistent Hashing
  - Rendezvous Hashing
- Location-independent addressing

### Distributed Apps (dApps)

https://blockchainhub.net/decentralized-applications-dapps/

Decentralized applications (dApps) are applications that run on a P2P network of computers rather than a single computer. dApps, have existed since the advent of P2P networks. They are a type of software program designed to exist on the Internet in a way that is not controlled by any single entity.

Decentralized applications don’t necessarily need to run on top of a blockchain network. BitTorrent, Popcorn Time, BitMessage, Tor, are all traditional dApps that run on a P2P network, but not on a Blockchain (which is a specific kind of P2P network).

As opposed to simple smart contracts, in the classic sense of Bitcoin, that sends money from A to B, dApps have an unlimited number of participants on all sides of the market.

#### Difference between dApps & Smart Contracts

dApps are a ‘blockchain enabled’ website, where the Smart Contract is what allows it to connect to the blockchain. The easiest way to understand this is to understand how traditional websites operate.

The traditional web application uses HTML, CSS and Javascript to render a page. It will also need to grab details from a database utilizing an API. When you go onto Facebook, the page will call an API to grab your personal data and display them on the page.

**Traditional websites: Front End → API → Database**

dApps are similar to a conventional web application. The front end uses the exact same technology to render the page. The one critical difference is that instead of an API connecting to a Database, you have a Smart Contract connecting to a blockchain.

**dApp enabled website: Front End → Smart Contract → Blockchain**

As opposed to traditional, centralized applications, where the backend code is running on centralized servers, dApps have their backend code running on a decentralized P2P network. Decentralized applications consist of the whole package, from backend to frontend. The smart contract is only one part of the dApp.

dApps can have frontend code and user interfaces written in any language (just like an app) that can make calls to its backend. Furthermore, its frontend can be hosted on decentralized storage such as Swarm or IPFS.

For an application to be considered a dApp in the context of Blockchain, it must meet the following criteria:

- Application must be completely open-source  
  It must operate autonomously, and with no entity controlling the majority of its tokens. The application may adapt its protocol in response to proposed improvements and market feedback, but the consensus of its users must decide all changes.

- Application’s data and records of operation must be cryptographically stored  
  must be cryptographically stored in a public, decentralized blockchain in order to avoid any central points of failure.

- Application must use a cryptographic token  
  (Bitcoin or a token native to its system) which is necessary for access to the application and any contribution of value from (miners/farmers) should be rewarded with the application’s tokens.

- Application must generate tokens  
  according to a standard cryptographic algorithm acting as a proof of the value, nodes are contributing to the application (Bitcoin uses the Proof of Work Algorithm).

?? DApps use public blockchain for data and records of operation. What about log files?

Dapps use distributed file system and

#### DApp Development Kits

Truffle - https://truffleframework.com/  
Smart contract building and testing.

Metamask - https://metamask.io/  
browser extension to run etherium dapps.

### Distributed Autonomous Organization (DAO)

https://www.coindesk.com/information/what-is-a-dao-ethereum/

The goal is form a leaderless company, program rules at the beginning about how members can vote and how to release company funds and then... let it go.

There are a few ways that The DAO intended to improve on the governance of today's organizations:

- Anyone with internet access could hold DAO tokens or buy them

- DAO creators could set whatever rules they voted on.

In abstract, DAOs function similarly. They rely on smart contracts, or pre-programmed rules that describe what can happen in the system.

---

## Blockchain Critisisms and Negative Reviews

#### External events and smart contracts

https://www.coindesk.com/three-smart-contract-misconceptions/

Reacting to external events:

A blockchain is a consensus-based system, meaning that it only works if every node reaches an identical state after processing every transaction and block.

Everything that takes place on a blockchain must be completely deterministic, with no possible way for differences to creep in. The moment that two honest nodes disagree about the chain's state, the entire system becomes worthless.

Now, recall that smart contracts are executed independently by every node on a chain. Therefore, if a smart contract retrieves some information from an external source, this retrieval is performed repeatedly and separately by each node. But because this source is outside of the blockchain, there is no guarantee that every node will receive the same answer.

Perhaps the source will change its response in the time between requests from different nodes, or perhaps it will become temporarily unavailable. Either way, consensus is broken and the entire blockchain dies.

(Use of Oracles to push data into the blockchain as solution)

Causing external events:

When it comes to smart contracts causing events in the outside world, a similar problem appears. For example, many like the idea of a smart contract which calls a bank's API in order to transfer money. But if every node is independently executing the code in the chain, who is responsible for calling this API?

(Trusted service used to handle the event)

#### Slow transactions

https://datafloq.com/read/why-bitcoin-will-fail-what-will-come-next/3691?imm_mid=0f6ccf&cmp=em-na-na-na-newsltr_fintech_20171002

#### Blockchain is hard

https://medium.com/@jimmysong/why-blockchain-is-hard-60416ea4c5c

#### Smart Contracts Security

Smart contracts are programs which use data from the blockchain. They have internal blockchains (?) for internal data (encapsulation).

Security of the data inside smart contracts is an issue? Visible to anyone with access to the blockchain?

#### Ethereum DAO hack

Smart contacts are not concurrent. But they are reentrant. Ethereum DAO hack. \$50M.

http://hackingdistributed.com/2016/07/13/reentrancy-woes/

https://github.com/ConsenSys/smart-contract-best-practices/blob/master/docs/known_attacks.md

Do not perform external calls in contracts. If you do, ensure that they are the very last thing you do. If that's not possible, use mutexes to guard against reentrant calls. And use the mutexes in all of your functions, not just the ones that perform an external call.

#### Ambiguity in Smart Contracts

https://www.ibtimes.co.uk/pwc-blockchain-expert-pinpoints-sources-ambiguity-smart-contracts-1575778

## Tools for developing blockchain (Ethereum):

- Ganache - Wallet and simulator for ethereum network and apis

- Bitcoin-q - Comes with Bitcoin client.

- Ethereum wallet - Official wallet

- Metamask - Ethereum wallet

- Coinbase - Big, stable Crypto trading company.

## BlockChains

- **Bitcoin** - Original. Largest market cap. Slow. TPS=7. Concensus = POW (Proof of work)

- **Ethereum** - Open-source, blockchain platform, Solidity, Dapps. Slow. TPS=20. POW.

  - ETH. ERC20 tokens - Standard for custom tokens.

- **Hyperledger** - Private blockchain

  - <https://blockgeeks.com/guides/hyperledger-vs-ethereum/>

  - Fabric. Enterprise blockchain

## DAPPS - Distributed Apps

Example Dapps:

- Exchanges

- Gambling sites

## Tokens

- **Bitcoin**

- **Ether** - Ethereum bc token

- **ERC20** - Tokens based on Ethereum. Can be created, managed by creating a smart contract.

  - Exchanges need to write custom code to talk to your contract to handle the tokens.

  - Wallet software also.

  - ERC20 is a standard for tokens on ethereum to make them easier to manage. 6 mandatory functions and 3 optional.

## Advanced Ledger Features

<https://developers.ripple.com/xrp-ledger-overview.html#modern-features-for-smart-contracts>

A sample of advanced features in the XRP Ledger:

- `Payment Channels` allow asynchronous balance changes as fast as you can create and validate signatures.

- `Escrow` locks up XRP until a declared time passes or cryptographic condition is met.

- `DepositAuth` lets users decide who can send them money and who can't.

- A `Decentralized Exchange` lets users trade obligations and XRP on-ledger.

- `Invariant Checking` provides an independent layer of protections against bugs in transaction execution.

- `Amendments` provide smooth upgrades to the existing feature set, so the technology can continue to evolve without fracturing the ecosystem or causing uncertainty around times of transition.

- `Interledger` - Interledger is an open protocol suite for sending payments across different ledgers. Like routers on the Internet, connectors route packets of money across independent payment networks. The open architecture and minimal protocol enable interoperability for any value transfer system. Interledger is not tied to any one company, blockchain, or currency.

## Payment channels and Atomic Transactions

<https://coincentral.com/exchange-union-beginner-guide/>

### Payment Channels

> Payment channels provide an instant way to transfer digital assets off-chain between two parties. The transactions are only recorded on the blockchain when the payment channel is first opened and when it’s closed. You can think of it as updating balances on both ends of the channel for each transfer. Once you close the payment channel, both parties get their respective final balances.
>
> Payment channels are trustless – any disputes are resolved automatically through cryptography. And, transfers using them are secured by the underlying blockchain making them as reliable as exchanges on the blockchain itself.
>
> Bitcoin’s Lightning Network and Ethereum’s Raiden Network are two of the most popular examples of payment channels.
>
> Exchange Union utilizes Hashed Timelock Contracts (HTLCs) when connecting payment channels between exchanges. These contracts allow the platform to set-up XU nodes as trust-less intermediaries to route transfers through payment channels to multiple parties. This prevents exchanges from having to open up payment channels with every participant on the network. Instead, they can use a route of channels to facilitate transfers to their final destination.
>
> Each platform participating in trades through Exchange Union needs to have an XU node and connect it to at least one other exchange for each digital asset with a payment channel.

### Atomic Transactions

> Cross-chain atomic swaps on payment channels
>
> A trade always consists of two transfers across payment channels. Because of this, there’s an inherent risk of one party behaving dishonestly. After receiving their part of the trade, the first party could simply not transfer their funds to the other party. Via atomic swaps, it’s cryptographically ensured that both sides of the trade have to happen successfully. This makes trading on Exchange Union secure & trustless.
>
> Atomic swaps use modified HTLCs to enable trades across payment channels. For example:

    - Sally wants to trade her Litecoin for Ethereum Classic on Exchange A.
    - Bob wants to trade his Ethereum Classic for Litecoin on Exchange B.
    - Exchange A sends Sally’s funds to Exchange B on the Litecoin payment channel.
    - Exchange B sends Bob’s funds to Exchange A on the Ethereum Classic payment channel.
    - The unique HTLC guarantees that both sides of the trade happen successfully.
