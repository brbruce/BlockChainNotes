# AWS Marketplace: Ethereum Development and Training Suit by Techlatest.net

<!-- TOC -->

- [Overview](#overview)
- [Configuration](#configuration)
  - [Restarting VM and session after stopping and starting](#restarting-vm-and-session-after-stopping-and-starting)
  - [Useful Commands](#useful-commands)
  - [NPM installations on server](#npm-installations-on-server)
- [Video 3: Running Ethereum HelloWorld demo](#video-3-running-ethereum-helloworld-demo)
- [Video 4: Petshop Overview](#video-4-petshop-overview)
- [Video 5: Petshop Development and Deployment](#video-5-petshop-development-and-deployment)

<!-- /TOC -->

## Overview

<http://www.techlatest.net/products/ethereum_development_and_traning_suit/>

<http://www.techlatest.net/support/ethereum_developer_kit/>

<https://aws.amazon.com/marketplace/library?ref_=header_user_your_software>

Login: bbawsjunk1 (user)

Region: N. Virginia

EC2 - 1 \* t2.large

Cost: ~ $0.257 / hr = $67/month

---

## Configuration

Go to <https://aws.amazon.com/marketplace/library?ref_=header_user_your_software> and click "Launch More Software".

Click "Continue to Launch" button in upper right corner.

Use the following settings:

- Launch From Website
- t2.large
- default vpc
- default subnet settings
- Create new Security group settings with ssh and rdp access from My IP only.
- Create new Key Pair and save the private key in a secure file system.

Launch, and view the instance in the EC2 console.

In the EC2 console, to get instructions for SSH, click the Connect button at the top of the Instances page. You need to configure Putty with the private key file location, the username of "ubuntu" (Per the usage instructions below), and the public DNS address.

NOTE: To use Putty, you need to convert the pem private key file to ppk format using PuttyGen. Just load the pem file, and save as Putty key ppk extension. Then use that one.

    In gitbash shell:
    ssh -i "techlatest_ethereum.pem" ubuntu@ec2-34-239-148-211.compute-1.amazonaws.com

    In putty:
    techlatest_ethereum.ppk

Next, log in and change the ubuntu user's password:

    sudo passwd ubuntu

Next, start Remote Desktop Connection in Windows menu and enter userid ubuntu and new password. Use module type "sesman-Xvnc".

Now you will see a desktop environment.

---

Follow below instructions to enable remote desktop login (RDP) after starting the instance:

1. Login to the instance using SSH via key based authentication. Use "ubuntu" as userid (refer https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html for details on how to connect using putty/ssh)

2. Once connected using ssh/putty, run below command to set the password for "ubuntu" user on the terminal sudo passwd ubuntu

3. Once the password is set for ubuntu user, from your local windows machine, goto start menu.

4. On the start menu, search and select "remote desktop connection" .

5. In the "remote desktop connection" wizard, provide public IP of your instance and click connect.

6. In the displayed window, provide "ubuntu" as userid and password set in step 2 above.

7. Now you are connected to the desktop environment of Ethereum devkit where you can access out of box environment for Ethereum development.

To learn more on how to use Ethereum development kit, please visit http://techlatest.net/support/ethereum

---

### Restarting VM and session after stopping and starting

Go to <https://console.aws.amazon.com/ec2/home?region=us-east-1#Instances:sort=instanceId> and login with AWS login id (j1). Start instance named "TechLatest"

Copy public DNS name (like "ec2-3-215-177-74.compute-1.amazonaws.com"). This changes each time the server restarts.

Start Putty. In Session tab > hostname = "ubuntu@" + the public DNS name.

In Connection > SSH > Auth tab > private key file = the saved putty private key file for techlatest. Connect via SSH to test server is running.

Start Remote Desktop Connection. Enter hostname "ec2-3-215-177-74.compute-1.amazonaws.com" (or new public DNS) and username "ubuntu". Password in LP under TechLatest. Or find the TechLatest.rdp file and double-click.

For Surface Pro, change desktop resolution to 1680x1050 before starting RDP.

### Useful Commands

SSH to server:

    ssh -i "techlatest_ethereum.pem" ubuntu@ec2-34-239-148-211.compute-1.amazonaws.com

scp file from server:

    tar -cvf ethereum.tar --exclude node_modules --exclude quorum-examples/quorum/* --exclude quorum-examples/examples/* ethereum

    scp -i "/c/Users/publi/OneDrive/Documents/_Tech Info/PublicPrivateKeys/TechLatest_Ethereum_Training_AWS_Keys/techlatest_ethereum.pem" -r ubuntu@ec2-3-215-177-74.compute-1.amazonaws.com:/home/ubuntu/Desktop/ethereum.tar .

From frostbite. Do not use quotes around the private key file name, and don't use the -r parameter:

    scp -i /C/Users/Brian/SkyDrive/Documents/_Tech\ Info/PublicPrivateKeys/TechLatest_Ethereum_Training_AWS_Keys/techlatest_ethereum.pem ubuntu@ec2-3-80-6-118.compute-1.amazonaws.com:/home/ubuntu/Desktop/ethereum/demos/pet-shop-tutorial/petshop.tar .

To ssh, do not use quotes around the private key file name. Also, specify the user and host before the -i param instead of using the -l param.

    ssh ubuntu@ec2-3-80-6-118.compute-1.amazonaws.com -i /C/Users/Brian/SkyDrive/Documents/_Tech\ Info/PublicPrivateKeys/TechLatest_Ethereum_Training_AWS_Keys/techlatest_ethereum.pem

### NPM installations on server

    ubuntu@ip-172-31-71-200:~/Desktop/ethereum/demos/helloworld_demo$ npm -g list --depth=0
    /home/ubuntu/.nvm/versions/node/v9.8.0/lib
    ├── ethereumjs-testrpc@6.0.3
    ├── ganache-cli@6.1.0
    ├── npm@5.6.0
    └── truffle@4.1.3

ethereumjs-testrpc has been renamed to ganache-cli, which is also installed.

---

## Video 3: Running Ethereum HelloWorld demo

Start the test Ethereum network, and deploy contracts in the 'helloworld_demo' project to the network.

ssh to server

    cd ~/Desktop/ethereum/demos/helloworld_demo

Start `testrpc`:

    ubuntu@ip-172-31-71-200:~/Desktop/ethereum/demos/helloworld_demo$ testrpc

    EthereumJS TestRPC v6.0.3 (ganache-core: 2.0.2)

    Available Accounts
    ==================
    (0) 0xe9d0a27b23fd3f9ca55b49b5208bb290001d8697
    (1) 0xf03f18568aec0c35a0295063ccce42ab3c8069bf
    ...

    Private Keys
    ==================
    (0) e583a3f87d043ebe4e3d7942572ae0e08be776cb282fa41b4dc3285887266120
    (1) 158df97c8c6b010502a3c2f9db83dc4061b5658259a981897efb75a8daacd7f5
    ...

    HD Wallet
    ==================
    Mnemonic:      emerge monkey melt plunge village soul this mango either symbol resist alley
    Base HD Path:  m/44'/60'/0'/0/{account_index}

    Listening on localhost:8545

Deploy contracts to the test network:

    ubuntu@ip-172-31-71-200:~/Desktop/ethereum/demos/helloworld_demo$ truffle migrate

    Using network 'development'.

    Running migration: 1_initial_migration.js
    Deploying Migrations...
    ... 0x11ec35cab9edb1aed89ca4ab32b0b4fe1a613d99da514ddeec655a71da4cad3a
    Migrations: 0xd615ff47c80ebc44d2218c905d9e33c0438c0824
    Saving successful migration to network...
    ... 0x46d410104fb33dc7ce82785e64bf51b307b658319c643af3ab9003110492fb42
    Saving artifacts...
    Running migration: 2_deploy_contract.js
    Deploying ConvertLib...
    ... 0x7851a0b97567504f59d2fe98cf6d3af5aef8490c2821d35b3ed5ee884c7841d5
    ConvertLib: 0xf31b7bebe3568bb0e608446c17c456da382c4543
    Linking ConvertLib to MetaCoin
    Deploying MetaCoin...
    ... 0x4c4358c0d7444791225b91afef564232bfd4454c4edf5413ffe2ce7d7dca5aca
    MetaCoin: 0xee09af340e90fc290bc0a425ed9f30e5ab3d62ae
    Saving successful migration to network...
    ... 0x5bff3796e39e9ab13a0ed70b1796830f294f2345057e5599e4c0e1ef60844523
    Saving artifacts...

Output in testrpc logs:

    net_version
    eth_accounts
    eth_accounts
    net_version
    net_version
    eth_sendTransaction

    Transaction: 0x11ec35cab9edb1aed89ca4ab32b0b4fe1a613d99da514ddeec655a71da4cad3a
    Contract created: 0xd615ff47c80ebc44d2218c905d9e33c0438c0824
    Gas usage: 269607
    Block Number: 1
    Block Time: Wed Jun 05 2019 22:27:47 GMT+0000 (UTC)

    eth_newBlockFilter
    eth_getFilterChanges
    eth_getTransactionReceipt
    eth_getCode
    eth_uninstallFilter
    eth_sendTransaction

    Transaction: 0x46d410104fb33dc7ce82785e64bf51b307b658319c643af3ab9003110492fb42
    Gas usage: 41981
    Block Number: 2
    Block Time: Wed Jun 05 2019 22:27:47 GMT+0000 (UTC)

    ...

    eth_getTransactionReceipt

Now the contracts in the helloworld_demo project are deployed.

Start the truffle console from the commandline so we can query and issue commands:

    ubuntu@ip-172-31-71-200:~/Desktop/ethereum/demos/helloworld_demo$ truffle console
    truffle(development)>

Some commands:

    // get accounts
    web3.eth.accounts

    // Check default account in console session
    web3.eth.coinbase (This will default to the first account in the accounts list, and is where the tx.origin value comes from.)

    web3.eth.getBalance(web3.eth.coinbase)

    // get reference to deployed contract
    var metacoin;
    MetaCoin.deployed().then(function(deployed) {metacoin = deployed;});

    // get balance of account 0
    metacoin.getBalance.call(web3.eth.accounts[0]);

    // send coins
    var account0 = web3.eth.accounts[0];
    var account1 = web3.eth.accounts[1];
    metacoin.sendCoin(account1, 1000, {from: account0});
    metacoin.getBalance.call(account0);

List accounts:

    truffle(development)> web3.eth.accounts
    [ '0xe9d0a27b23fd3f9ca55b49b5208bb290001d8697',
    '0xf03f18568aec0c35a0295063ccce42ab3c8069bf',
    '0x6820a02e8aa1cb1c8d55f1bf79fa9cc334679807',
    '0x9d9f0544781c7b5e2d8c663a232bbb67eb9dcb5b',
    '0xc5f91e923e7e6d7fece9e0d7f61c1c67c159a036',
    '0xa816449acb77c6012c91d6539f59cb3b6e971ed8',
    '0xe7ae47ff96eec29649434e2969185ed6ea0715f4',
    '0x0de6563bee6d53d4664f3d0503843361a94afb08',
    '0x3e1ea6067081c533316c46faf1dbe417e65afa00',
    '0xf1fcedf9987c50d762d9f169a6866ddf8956d6ce' ]

Run the js to assign the deployed MetaCoin contract instance to `metacoin` variable:

    truffle(development)> var metacoin;
    undefined

    truffle(development)> MetaCoin.deployed().then(function(deployed) {metacoin = deployed;});
    undefined

Check the value of metacoin after:

    truffle(development)> metacoin
    TruffleContract {
    constructor:
    { [Function: TruffleContract]
        _static_methods:
        { setProvider: [Function: setProvider],
            new: [Function: new],
            at: [Function: at],
            ...

Use the contract instance to check the balance of account 0:

    truffle(development)>     metacoin.getBalance.call(web3.eth.accounts[0]);
    BigNumber { s: 1, e: 4, c: [ 10000 ] }

Send coins from acct 0 to acct 1:

    truffle(development)> var account0 = web3.eth.accounts[0];
    undefined

    truffle(development)> var account1 = web3.eth.accounts[1];
    undefined

    truffle(development)> metacoin.sendCoin(account1, 1000, {from: account0});
    { tx: '0x2e37dc20d39bcbd936ec61323eb0d328ba1bfe4016a0afd5556c4880923a1940',
    receipt:
    { transactionHash: '0x2e37dc20d39bcbd936ec61323eb0d328ba1bfe4016a0afd5556c4880923a1940',
        transactionIndex: 0,
        blockHash: '0x0abba4cbee3deaba27b83b8aa1e10246f966fc1a0c43ac9b1debc87137629714',
        blockNumber: 6,
        gasUsed: 49196,
        cumulativeGasUsed: 49196,
        contractAddress: null,
        logs: [],
        status: 1 },
    logs: [] }

In the network log:

    eth_sendTransaction

    Transaction: 0x2e37dc20d39bcbd936ec61323eb0d328ba1bfe4016a0afd5556c4880923a1940
    Gas usage: 49196
    Block Number: 6
    Block Time: Wed Jun 05 2019 23:21:00 GMT+0000 (UTC)

    eth_getTransactionReceipt

## Video 4: Petshop Overview

## Video 5: Petshop Development and Deployment

Petshop - Download the Petshop Truffle box
