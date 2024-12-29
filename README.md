# Blockchain-Technologies---Assignment-1
Overview
This project involves developing a smart contract capable of receiving and managing Ether tokens. The assignment also includes configuring the environment with Web3.js and Ganache, deploying the smart contract, and interacting with it using Metamask.

Features
Smart Contract Functionalities:

Receive Ether tokens.
Check the smart contract balance.
Withdraw all Ether tokens by the owner.
Environment Configuration:

Web3.js setup.
Integration with Ganache and/or any public Testnet.
Deployment:

Smart contract deployed to Ganache and/or a public Testnet.
Interaction:

Execute smart contract functions via Metamask and Web3.js.
Prerequisites
Ganache: For local blockchain environment.
Metamask: Browser-based Ethereum wallet.
Web3.js: Ethereum JavaScript API library.
Node.js: Required to run Web3.js.
Setup Instructions
Clone the repository:

bash
Copy code
git clone <repository_url>
cd <repository_name>
Install dependencies:

bash
Copy code
npm install
Run Ganache:

Open Ganache and start a workspace.
Deploy the Smart Contract:

Use Truffle or Remix IDE to deploy the contract to Ganache.
Configure Metamask:

Connect Metamask to the Ganache blockchain.
Interact with the Contract:

Use Web3.js scripts or a front-end interface to call the contract's functions.
Usage
Check Balance: Run the function getBalance() to check the contract balance.

Withdraw Funds: Only the owner can call the withdraw() function to retrieve the Ether tokens.

Demo
Screenshots
Deployment to Ganache
Metamask interaction
Function calls
GIF
Showing contract deployment and interaction.
Examples
Sample Web3.js Script:
javascript
Copy code
const Web3 = require('web3');
const web3 = new Web3('http://127.0.0.1:7545'); // Ganache URL
const contractABI = []; // Add contract ABI
const contractAddress = ''; // Add contract address

const contract = new web3.eth.Contract(contractABI, contractAddress);

// Call contract functions here
License
This project is licensed under the MIT License. See the LICENSE file for details.

References
Web3.js Documentation
Ganache
Metamask Setup
