# Blockchain Devt Tips

---------------------------------------------------------------------

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

- **TRON** - Fork of Eth.  Fast. TPS=2000. POS (Proof of stake).  Less decentralized.  27 Elected block producers.

  - TRX token.  USDT token is USD stablecoin issued by Tether.

- **EOS** - Fast.  TPS=4000.  POS.  21 block producers.

- **Ripple** - Fast. TPS=1500. Trusted Validators.

  - <https://www.investinblockchain.com/what-is-ripple/>

  - XRP token. Designed for financial institutions.  Centralized.

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

## Exchanges

<https://www.bti.live/reports-april2019/>

Real volume excluding wash sales:

- **1) Binance** - $821M 24hr volume, not BTI verified

- **3) Upbit** - $436M, BTI verified

- **10) Coinbase** - $154M, BTI verified

## Centralized vs Decentralized Exchanges

<https://hacken.io/decentralized-and-centralized-exchanges-advantages-vs-disadvantages-aa9a27da4584/>

<https://coinsutra.com/best-decentralized-exchanges-dex/>

- IDEX



## How to buy and trade crypto

### Security

- 2FA - Google Authenticator or Authy
  - Recovery key - Save the input string when registring the 2FA, in case you lose your phone.

- Back Phrase - Seed phrase.  12 random words used to generate tree of private keys.  Can be used to regenerate all private keys.  Used as backup for a wallet.

- Hardware wallet - Don't store funds on the exchange.  Buy hardware wallet like Ledger Nano S.
  - Ledger Nano S.

- Whitelist of public addresses which are authorized to receive funds.

- Antiphishing code word - Used on emails to prove the sender is the exchange.

- Don't keep funds online in exchanges.  Transfer to private wallet and safeguard the app with long passwords or pins and 2FA, and store backups of the keys on encrypted USB drive stored in bank safe deposit box.

### Crypto Wallets

Hot vs Cold - Online wallet vs offline.  

- Paper - Cold
- Hardware - Cold
- Desktop - Hot, keys are local
- Mobile - Hot, keys are local
- Browser - Hot, keys online

HD Wallets - Hierarchical Deterministic. Uses 12 word master seed key to generate new private/public keys.  Only need to back up the master seed key. (BIP32)  SHA-256.

- <https://coinsutra.com/hd-wallets-deterministic-wallet/>

Multicurrency wallets have one private key for each coin type.  (Gets hard to manage)

### Fees and expenses

Coinbase charges 0.5% spread on all transactions, plus a fee.  Fee is greater of flat fee or variable % (4%).  Best rate if you do direct transfer to/from bank acct.

<https://support.coinbase.com/customer/portal/articles/2109597-buy-sell-bank-transfer-fees>

Transfer fees - You will get charged a fee whenever you transfer coins, even between your own wallets.

--------------------------------------------------------------------

## My Exchanges and Wallets

All wallet information is available in LastPass.

### CoinBase Exchange

- Popular exchange.

- Nice interface, simple.  Shows favorite coins with prices and graphs.

- Shows amounts in USD (easier to understand)

- Has reports and tax info.

- Bad - Asks for bank login and password.

- Bad - Cannot exchange coin types directly.  Must sell one coin and then buy another coin, which has more transaction fees.

- Bad - Does not take Credit card.  Bank acct and Debit card only.

- Bad - No email confirmations.

- Fees

  - Purchase: Used $750 to buy BTC using debit card.  Received 0.13907594 BTC ($721.22) ($5,185.80/BTC).  Fee was $28.78. (Cheaper than Binance)

  - Transfer: Sent 0.002 BTC ($10.50) to Trust Wallet.  Fee was 0.00008679 BTC ($0.46).  The fee is fixed, regardless of transfer amount.
    - Fee is added to the amount sent.  Sent 0.002.  Deducted 0.00208679.  Received 0.002. (Cheaper than Binance)

### Binance Exchange

- One of the largest by volume and capitalization.

- Advanced interface, has trading screens.

- Uses Simplex for bank integration.

- Can exchange coins directly.

- Email confirmations.

- Bad - Not much USD conversion info.

- Bad - No reports or tax info.

- Fees

  - Purchase: Bought $750 of bitcoin.  Received 0.13730614 BTC (~$712.04).  Fee was ~$37.95. (More expensive than CoinBase)

  - Transfer: Sent 0.002 BTC (~$10.50) to Trust Wallet.  Fee was 0.0005 BTC (~$2.70).  The fee is fixed, regardless of transfer amount.
    - Fee is deducted from the amount sent.  Sent 0.002 but only received 0.0015.

### Guarda Wallet

- Only loads keys while running.  (Not sure if this is actually more secure or not)

- Backup file includes encrypted keys.

- Can exchange coins (Uses Guarda exchange)

- Bad - Cannot set favorite coins.  See entire list. (Can delete all unused currencies to clean up list)

- Bad - Cannot buy coins directly.

- Bad - Not much market data or graphs.

### Trust Wallet

- Official wallet for Binance.  

- Uses HD back phrase to generate keys and backup and restore.

- Can set favorite coins list

- Can view coin graph and market data.

- Can buy coins using USD.  Uses Simplex (Same as Binance)

- Bad - Cannot exchange coins