# TipJar
TipJar is a simple Ethereum smart contract that allows users to send tips along with a name and a message. The tips are collected by the contract owner. This repository includes the Solidity smart contract code and a Hardhat script to deploy and interact with the contract.

## Table of Contents
+ Installation
+  Usage
+  Smart Contract
+  ardhat Script
+  ontributing
+  icense
   
### Installation
To use this project, you'll need to have Node.js and Hardhat installed.

1. Clone the repository:
   git clone https://github.com/your-username/tipjar.git
   cd tipjar
   
3. Install dependencies:
    npm install

### Usage
Deploying the Contract
1. Install the dependencies:

   npm install
  
2. Open two additional terminals in your VS Code.

3. In the second terminal, start the Hardhat local blockchain:

    npx hardhat node

4. In the third terminal, deploy the contract to the local blockchain:

    npx hardhat run --network localhost scripts/deploy.js

5. In the first terminal, start the front-end application:

     npm run dev
   
6.  After this, the project will be running on your localhost, typically at http://localhost:3000/.

   
### Interacting with the Contract
1. Run the provided script to send tips and log balances and tips
   npx hardhat run scripts/interact.js --network <network-name>

## Example Output
  At [timestamp], name: Amit, address: [address], message: Great tip!
  At [timestamp], name: Ravi, address: [address], message: Thanks for the info!
  At [timestamp], name: Ileana, address: [address], message: Keep it up!

# Smart Contract
The TipJar smart contract allows users to send tips to the contract owner with a name and a message.

#### Tip Struct
      struct Tip {
          string name;
          string message;
          uint256 timestamp;
          address from;
      }
      
## Functions
+ sendTip(string memory name, string memory message) public payable: Allows users to send tips. The tip amount must be greater than 0 ether.
+ getTips() public view returns (Tip[] memory): Returns an array of all tips received.

# Hardhat Script
The Hardhat script (scripts/interact.js) deploys the TipJar contract, simulates sending tips from multiple addresses, and logs the relevant details before and after sending tips.

## Functions
+ getBalances(address): Fetches the balance of an Ethereum address in Ether.
+ consoleBalances(addresses): Logs the balances of multiple Ethereum addresses.
+ consoleTips(tips): Logs the details of tips.

## Contact
For any questions or suggestions, feel free to open an issue or contact the repository owner.

Mail - vermashiv1910@gmail.com










  
