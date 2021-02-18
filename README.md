# Multi-Blockchain Wallet in Python

## Overview

This repo will show how to create and send Testnet BTCTEST and ETH coins to designated accounts using Python code and various publicly available software tools and packages as well as Python packages. 

## Dependencies

- PHP must be installed on your operating system (any version, 5 or 7). Please click this link for PHP installation instructions. [PHP Installation Guide](https://github.com/camdorazio/wallet/blob/main/HD_Wallet_Derive_Install_Guide.md)
- The hd-wallet-derive tool. Follow the instructions in this guide to install/clone. [HD-Wallet-Derive Installation Guide](https://github.com/camdorazio/wallet/blob/main/HD_Wallet_Derive_Install_Guide.md)
- bit for Python. [bit](https://pypi.org/project/bit/)
    - Link for bit resource guide. [bit resource guide](https://ofek.dev/bit/)
- web3.py Python Ethereum library. Follow the instructions in this guide to install/clone. [HD-Wallet-Derive Installation Guide](https://github.com/camdorazio/wallet/blob/main/Blockchain_TX_Install_Guide.md)
    - Link to web3.py documentation. [web3.py](https://web3py.readthedocs.io/en/stable/index.html)
- A custom ETH Proof of Authorty blockchain. You can create one by following these instructions. [POA](https://github.com/camdorazio/Proof-of-Authority-Dev-Chain)
- MyCrypto applcation. Follow this link to download the application. [MyCrypto download](https://download.mycrypto.com/)
- GitBash Follow this link to download the application. [GitBash download](https://git-scm.com/downloads)
- Jupyter Lab (optional as you can use the same code in Python) [Jupyter Install instructions](https://jupyter.org/install)

# Generating wallets and addresses using HD-Wallet-Derive

- First you will need to get a mneumonic and generate some wallet addresses. You can use this website to generate the mneumonic for you. [Generate Mneumonic](https://iancoleman.io/bip39/)

- Once you generate the mneumonic you will have access to multiple coin wallet addresses. Write down this phrase in order and store it in a safe place. Do not share this phrase with anyone, treat it like your banking password. It's highly recommended that you create a .env file to store the mneumonic and pass in the mneumonic into your Python code using python-dotenv. [python-dotenv](https://pypi.org/project/python-dotenv/)

![python-dotenv code](./Screenshots/ImportMneumonic.png "python-dotenv code")

- Here is the sample code to derive your wallet addresses:

![derive wallets](./Screenshots/derivewallets.png "derive wallets")

- You will have access to all available coins using the mneumonic. For this excercise, we will only focus on BTCTEST and ETH. We will now define a function just for these 2 coins.

![coins](./Screenshots/coins.png "coins")

# Code Snippets for BTCTEST and ETH transactions

## BTCTEST sample code and transactions
- 


