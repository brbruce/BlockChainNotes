# BlockChainNotes

7/2/2018
## Links
#### Ethereum Whitepaper
https://github.com/ethereum/wiki/wiki/White-Paper#applications

#### Blockchain Train Blog
http://decentralized.blog/catching-the-blockchain-train.html

#### Safari - Blockchain for dummies
https://www.safaribooksonline.com/library/view/blockchain-for-dummies/9781119365594/01_9781119365617-ffirs.xhtml

#### Bitcoin
https://bitcoin.org/en/developer-guide

#### Ethereum
https://github.com/ethereum/wiki/wiki/White-Paper  
https://media.consensys.net/the-state-of-the-ethereum-network-949332cb6895

#### Truffle IDE Ethereum
https://truffleframework.com/tutorials/ethereum-overview

----------

## Terms

Decentralized - Direct connection between users and providers.  No third party.  
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

### Consensus algorithms

https://hackernoon.com/a-hitchhikers-guide-to-consensus-algorithms-d81aae3eb0e3

In the world of crypto, consensus algorithms exist to prevent double spending. 
Proof-of-work - Mining  
Proof-of-stake - Minting, Forging  
DPOS  
Proof-of-authority  
Proof-of-weight  
Byzantine Fault Tolerance    
* PBFT - Centralized, permissioned  
* Federated BFT - good one  
* Directed Acyclic Graphs (DAGs) — aka the Blockchain Killers!


### Permissionless (Public) vs Permissioned (Federated) and Tokens
Only permissionless ledgers (public Blockchains like Bitcoin or Ethereum), need some sort of incentive mechanism to guarantee that block validators do their job according to the predefined rules. 

In permissioned (federated/consortium/private) distributed ledger systems, validators and block-creators may be doing their job for different reasons: i.e., if they are contractually obligated to do so. In permissioned environments, validators can only be members of the club and are manually and centrally controlled. 

**Permissioned ledgers, therefore, don’t need a token.** Also, please note that the term blockchain in the context of such ledgers is highly controversial.

### Tokens
https://blockchainhub.net/tokens/

* Intrinsic, Native or Built-in Tokens - of blockchains like Bitcoin, Ether, etc that serve as: (a) block validation incentives (‘miner rewards’); and (b) transaction spam prevention. The logic behind this is that if all transactions are paid, it limits the ability to spam.  

* Application Tokens - With Ethereum, tokens can now easily be issued on the application layer through smart contracts on the Ethereum Blockchain as so-called complex dApp tokens or complex DAO tokens.  

* Asset-backed tokens - that are issued by a party onto a blockchain for later redemption. They are the digital equivalent to physical assets. They are claims on an underlying asset (like the gold), that you need to claim from a specific issuer (the goldsmith). The transactions as tokens get passed between people are recorded on the blockchain. To claim the underlying asset, you send your token to the issuer, and the issuer sends you the underlying asset.  

### Consensus mechanism: Proof-of-work vs Proof-of-stake

POW - Use CPU and electricity to calculate hash of the next block.  Get a reward of 12.5 BTC/block + transaction fee.  Difficulty increases to maintain constant time to solve.  
POS - Less electricity required.  Next block assigned to user based on random or age-based, and size of user's stake.  No reward, only transaction fee.

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
Bitcoin - Not private.  Transparent, easy to trace.

### Wallets

https://masterthecrypto.com/guide-to-cryptocurrency-wallets/

### UTXO (bitcoin) vs Accounts (Ethereum)

https://ethereumbuilders.gitbooks.io/guide/content/en/design_rationale.html


----------

## Components
Distributed File System    
* Sia, Swarm, Storj  

Distributed Web  
* IPFS - Interplanetary File System  
    - Uses distributed hash table - Used for DNS, multicast, instant messaging, bittorrent.  
* Distributed Caching - https://en.wikipedia.org/wiki/Distributed_hash_table  
    - Consistent Hashing  
    - Rendezvous Hashing  
* Location-independent addressing  

#### Distributed Apps (dApps)

#### DApp Development Kits

Truffle - https://truffleframework.com/  
Smart contract building and testing.