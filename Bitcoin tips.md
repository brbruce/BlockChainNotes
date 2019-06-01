# Bitcoin Tools and Tips

## BitCoin Core & bitcoin-qt.exe

BitCoin Core is a blockchain app which lets you start a local node, but you need to download the entire chain.

It comes with a tool called `bitcoin-qt` which allows you to run a local chain, without needing to sync the entire bitcoin blockchain.

    bitcoin-qt -regtest - Local
    bitcoin-qt -testnet - Test net

<https://bitcoin.stackexchange.com/questions/37902/running-another-instance-of-bitcoin-qt-dedicated-to-testnet-regtest>