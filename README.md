# Gas Introduction

I created this readme to share what I've learned about gas concepts in Ethereum, covering transaction fees, gas prices, mining incentives, computational measures in transactions, and a step-by-step guide to sending a transaction in Ethereum’s test network.

## Table of Contents

1. [Introduction to Gas](#introduction-to-gas)
2. [Understanding Transaction Fees and Gas Prices](#understanding-transaction-fees-and-gas-prices)
3. [The Role of Nodes in Blockchain](#the-role-of-nodes-in-blockchain)
4. [Understanding Gas in Transactions](#understanding-gas-in-transactions)
5. [Hands-on: Sending an Ethereum Transaction](#hands-on-sending-an-ethereum-transaction)
6. [Conclusion](#conclusion)

## Introduction to Gas

When I inspect an Ethereum transaction, two terms quickly catch my eye: "transaction fee" and "gas price". Let me clarify what they are and why they matter.

## Understanding Transaction Fees and Gas Prices

- **Transaction Fee**: This is the amount rewarded to the block producer for processing the transaction. It's paid in Ether or GWei.
- **Gas Price**: This is the cost per unit of gas specified for the transaction, also defined in Ether or GWei. The higher the gas price, the greater the chance of the transaction being included in a block.

I learned that gas price should not be confused with gas. While gas refers to the computational effort required to execute the transaction, gas price is the cost per unit of that effort.

When I view transaction details, I can see further information including the `gasLimit` and `Usage by transaction`.

## The Role of Nodes in Blockchain

Blockchains are run by a group of different nodes, sometimes referred to as miners or validators, depending on the network. These miners are incentivized for running the blockchain by earning a fraction of the native blockchain currency for processing transactions.

- **Ethereum Miners**: Get paid in Ether.
- **Polygon Miners**: Get rewarded in MATIC, the native token of Polygon.

This remuneration encourages people to continue running these nodes.

## Understanding Gas in Transactions

In the context of transactions, gas signifies a unit of computational complexity.

- **Simple Transactions**: Sending Ether requires relatively small amounts of gas.
- **Complex Transactions**: Minting an NFT, deploying a smart contract, or depositing funds into a DeFi protocol demand more gas due to their complexity.

I found out that the total transaction fee can be calculated by multiplying the gas used with the gas price in Ether (not GWei):

Transaction Fee = Gas Used × Gas Price

Where:
- **Gas Used** is the amount of gas consumed by the transaction.
- **Gas Price** is the cost per unit of gas, typically measured in Ether.

For example, if a transaction uses 21,000 gas units and the gas price is 0.00000002 Ether per gas unit, the transaction fee would be:

Transaction Fee = 21,000×0.00000002 = 0.00042 Ether

## Hands-on: Sending an Ethereum Transaction

Making a transaction requires the payment of a transaction fee to the blockchain nodes processing that transaction. Let me take you through an example using the MetaMask extension, a popular Ethereum wallet.

### Steps to Send a Transaction:

1. **Open MetaMask** and click "Expand View".
2. Choose the account (Account 1) to use for the transaction.
3. Click on "Send".
4. Select "Transfer between my accounts".
5. Enter the account (Account 2) to send the Ether to, and the amount you wish to send.
6. Click "Next". MetaMask will automatically calculate the gas fee for you. The total amount to be paid is the sum of the Ether value you're sending and the gas fee.

### Optional Settings for Gas:

If you click the market link in MetaMask, you'll see optional settings for gas in the transaction.

**Why spend more gas?**
If many people are trying to process transactions simultaneously, the space on a given block becomes competitive. Gas prices increase to throttle and prioritize transactions during congestion.

7. Click "Confirm".

The transaction will now appear in the Activity tab of MetaMask. You can view the transaction details as shown below:

#### Account 1
![Account 1](https://github.com/jason-victor1/Gas-Intro/blob/main/Account1.png?raw=true)

#### Account 2
![Account 2](https://github.com/jason-victor1/Gas-Intro/blob/main/Account2.png?raw=true)

After a short while, the transaction gets processed, and you can view its details in a block explorer like Etherscan as shown below.

#### Etherscan
![Etherscan](https://github.com/jason-victor1/Gas-Intro/blob/main/etherscan.png?raw=true)

I have now sent my first blockchain transaction on the Sepolia test network!

## Conclusion

Knowing how to process transactions with MetaMask is vital and empowers me to interact with protocols on the Ethereum network and other blockchains. Understanding the details behind these transactions and the fundamental mechanics of blockchains is crucial for mastering blockchain technology.



