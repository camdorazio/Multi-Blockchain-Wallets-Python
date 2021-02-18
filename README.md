# Multi-Blockchain Wallet in Python

## Overview

This repo will show how to create and send Testnet BTCTEST and ETH coins to designated accounts using Python code and various publicly available software tools and packages as well as Python packages. The wallet creation will give you access to BTCTEST, ETH and hundreds of other coins!

## Dependencies/Requirements

- PHP must be installed on your operating system (any version, 5 or 7). Please click this link for PHP installation instructions. [PHP Installation Guide](https://github.com/camdorazio/wallet/blob/main/HD_Wallet_Derive_Install_Guide.md)
- The hd-wallet-derive tool. Follow the instructions in this guide to install/clone. [HD-Wallet-Derive Installation Guide](https://github.com/camdorazio/wallet/blob/main/HD_Wallet_Derive_Install_Guide.md)
- bit for Python. [bit](https://pypi.org/project/bit/)
    - Link for bit resource guide. [bit resource guide](https://ofek.dev/bit/)
- web3.py Python Ethereum library. Follow the instructions in this guide to install/clone. [HD-Wallet-Derive Installation Guide](https://github.com/camdorazio/wallet/blob/main/Blockchain_TX_Install_Guide.md)
    - Link to web3.py documentation. [web3.py](https://web3py.readthedocs.io/en/stable/index.html)
- A custom ETH Proof of Authorty blockchain. You can create one by following these instructions. [ETH custom POA](https://github.com/camdorazio/Proof-of-Authority-Dev-Chain)
- MyCrypto applcation. Follow this link to download the application. [MyCrypto download](https://download.mycrypto.com/)
- GitBash Follow this link to download the application. [GitBash download](https://git-scm.com/downloads)
- Jupyter Lab (optional as you can use the same code in Python) [Jupyter install instructions](https://jupyter.org/install)

# Generating wallets and addresses using HD-Wallet-Derive

- First you will need to get a mneumonic and generate some wallet addresses. You can use this website to generate the mneumonic for you. [Generate Mneumonic](https://iancoleman.io/bip39/)

- Once you generate the mneumonic you will have access to multiple coin wallet addresses. Write down this phrase in order and store it in a safe place. Do not share this phrase with anyone, treat it like your banking password. It's highly recommended that you create a .env file to store the mneumonic and pass in the mneumonic into your Python code using python-dotenv. [python-dotenv](https://pypi.org/project/python-dotenv/)

![python-dotenv code](./Screenshots/ImportMneumonic.png "python-dotenv code")

- Here is the sample code to derive your wallet addresses:

![derive wallets](./Screenshots/derivewallets.png "derive wallets")

- You will have access to all available coins using the mneumonic. For this excercise, we will only focus only on BTCTEST and ETH. We will now define a function just for these 2 coins.

![coins](./Screenshots/coins.png "coins")

- Finally, we will define a function to convert the private key string for each wallet into a Python object so we call call it when we create and send transactions.

![privatekeyobject](./Screenshots/privatekeyobject.png "privatekeyobject")

# Code Snippets for BTCTEST and ETH transactions

- In order to create and send transactions, we will need to define some functions for creating and sending.

![createandsend](./Screenshots/createandsend.png "createandsend")

## BTCTEST sample code and transactions
- First, you will need to fund one of your newly generated BTCTEST wallets with some Testnet BTC. You can obtain Testnet BTC from various faucets. For this example, I have obtained some BTCTEST from the following faucet ...
[BTCTEST testnet faucet](https://testnet.help/en/btcfaucet/testnet)

- Here is an example confirmation that your BTCTEST testnet BTC has been sent to your desgnated wallet.

![BTCTEST testnet faucet confirm](./Screenshots/TestnetBTCTESTfaucet.png "BTCTEST testnet faucet confirm")

- Next, we will check to ensure the transaction is on the Testnet blockchain network and ensure the transaction has been confirmed. This will tell us if we now have some BTCTEST coins. You can visit the following site and check either using the transaction hash (see above TX hash/Message from BTCTEST Testnet faucet confirmation) or entering your wallet address [Blockcypher](https://live.blockcypher.com/). Then you can check your wallet balances using Python code.

|![Wallet](./Screenshots/Blockcypherwallet.png "Wallet") | ![TX Hash](./Screenshots/BlockcypherTXHash.png "TX Hash")|
|:---:|:---:|
| Wallet | TX Hash |

![Python Wallet Balance](./Screenshots/PythonWalletBalance.png "Python Wallet Balance")

- Finally, we can create and send BTCTEST transaction between our newly created wallet addresses. Again, you can use BlockCypher to check the transaction status and wallet balances to ensure your transaction was processed and confirmed.

|![Python Code](./Screenshots/createandsendBTCTEST.png "Python Code") | ![BlockCypher](./Screenshots/BlockcypherReceiveWallet.png "BlockCypher")|
|:---:|:---:|
| Python Code | BlockCypher |
