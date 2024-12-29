# Blockchain-Technologies---Assignment-1

# EtherWallet Project

## Project Description
EtherWallet is a simple smart contract-based application developed in Solidity for managing an Ethereum wallet. It allows the owner to store Ether and withdraw the full balance at any time. The project includes deployment and interaction scripts written in JavaScript using the Web3.js library.

## Features
- **Deposit Ether**: Anyone can send Ether to the wallet.
- **Check Balance**: View the current balance of the contract.
- **Withdraw All Ether**: The contract owner can withdraw all funds.

## Project Files

### Smart Contract
**File**: `EtherWallet.sol`
```solidity
pragma solidity ^0.8.0;

contract EtherWallet {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    receive() external payable {}

    function getBalance() public view returns (uint) {
        return address(this).balance;
    }

    function withdrawAll() public {
        require(msg.sender == owner, "Only owner can withdraw");
        payable(owner).transfer(address(this).balance);
    }
}

Deployment Script
File: deploy.js


Deploys the EtherWallet smart contract to the Ganache local blockchain.
Interaction Script
File: interact.js

Interacts with the deployed contract, including checking the balance and withdrawing funds.
Configuration Files
package.json and package-lock.json specify dependencies and project metadata.


Dependencies
Node.js
Web3.js library (v4.16.0)
Ganache (local Ethereum blockchain)
Setup Instructions


Install Dependencies:
npm install
Start Ganache: Launch the Ganache local blockchain and note the RPC server URL (default: http://127.0.0.1:7545).

Deploy the Smart Contract:
node deploy.js
The deployment script will output the contract address.

Interact with the Smart Contract: Update the contract address in interact.js and run:
node interact.js
Example Output


Deploying:
Деплой осуществляется с аккаунта: 0xa7FE404aD9ECD3A4898c8518c7719b59f3aCa75f
Контракт задеплоен по адресу: 0x7f1A684ca3Bfe08B54415A407714B9aB35548B68

Interacting:
Баланс контракта: 1 ETH
Средства выведены!

Team Members:
Darkhan Serikov SE-2330
Akan Zhansarin SE-2322
Meiirzhan Zhumabek SE-2330
