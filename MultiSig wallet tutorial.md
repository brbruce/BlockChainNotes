# MultiSig Wallet Tutorial

--------------------------------------------------------------------

<https://medium.com/hellogold/ethereum-multi-signature-wallets-77ab926ab63b>

## Software used in the article

### gnosis multisig wallet contract

<https://github.com/gnosis/MultiSigWallet/blob/master/contracts/MultiSigWallet.sol>

NOTE: The gnosis site has own instructions for installing the Multisig wallet app, along with a web front end.  See <https://github.com/gnosis/MultiSigWallet> and <https://github.com/gnosis/MultiSigWallet/tree/master/dapp>.

### Parity Ethereum Client

Ethereum client program.  Download and install.

<https://github.com/paritytech/parity-ethereum/releases/tag/v2.4.5>

By default, Parity Ethereum runs a JSON-RPC HTTP server on port :8545 and a Web-Sockets server on port :8546. This is fully configurable and supports a number of APIs.

<https://wiki.parity.io/FAQ>

### XXXXX - Partity UI (Smart Contract loading)

Use to load and compile the smart contract for the multisig wallet.

NOTE: The UI no longer works.  They recommend using Remix IDE:

<https://remix.ethereum.org>

Or you can try using Truffle:

<https://github.com/trufflesuite/truffle>

### Parity Kovan Testnet

<https://kovan-testnet.github.io/website/>

Or you can try using Truffle Ganache-cli local test blockchain:

<https://github.com/trufflesuite/truffle>

---------------------------------------------------------------------------

## Testing procedure

Start Parity eth client locally, connecting to Kovan testnet.

    $ ./parity.exe --chain kovan

    2019-05-08 12:44:08  Starting Parity-Ethereum/v2.4.5-stable-76d4064a4-20190408/x86_64-windows-msvc/rustc1.33.0
    2019-05-08 12:44:08  Keys path C:\Users\publi\AppData\Roaming\Parity\Ethereum\keys\kovan
    2019-05-08 12:44:08  DB path C:\Users\publi\AppData\Local\Parity\Ethereum\chains\kovan\db\9bf388941c25ea98
    2019-05-08 12:44:08  State DB configuration: fast
    2019-05-08 12:44:08  Operating mode: active
    2019-05-08 12:44:08  Configured for Kovan Testnet using AuthorityRound engine
    2019-05-08 12:44:08  Listening for new connections on 127.0.0.1:8546.

Download multisig wallet contract

    wget https://github.com/gnosis/MultiSigWallet/blob/master/contracts/MultiSigWallet.sol

Download truffle.  

Prerequisites: Python

    https://www.python.org/downloads/release/python-373/

    npm install -g truffle