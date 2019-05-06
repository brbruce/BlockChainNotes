# Blockchain Tech Dev Notes

----------------------------------------------------------

## Tools for developing blockchain (Ethereum):

- Ganache - Wallet and simulator for ethereum network and apis

- Bitcoin-q - Comes with Bitcoin client.  

- Ethereum wallet - Official wallet

- Metamask - Ethereum wallet

- Coinbase - Big, stable Crypto trading company.

## BlockChains

- **Bitcoin** - Original.  Largest market cap.  Slow. TPS=7. Concensus = POW (Proof of work)

- **Ethereum** - Open-source, blockchain platform, Solidity, Dapps.  Slow. TPS=20. POW. 

  - ETH.  ERC20 tokens - Standard for custom tokens.

- **Hyperledger** - Private blockchain

  - <https://blockgeeks.com/guides/hyperledger-vs-ethereum/>

  - Fabric.  Enterprise blockchain

## DAPPS - Distributed Apps

Example Dapps:

- Exchanges

- Gambling sites

## Tokens

- **Bitcoin**

- **Ether** - Ethereum bc token

- **ERC20** - Tokens based on Ethereum.  Can be created, managed by creating a smart contract.

  - Exchanges need to write custom code to talk to your contract to handle the tokens.

  - Wallet software also.

  - ERC20 is a standard for tokens on ethereum to make them easier to manage.  6 mandatory functions and 3 optional.

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
>
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

