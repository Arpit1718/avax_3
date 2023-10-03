## Module 3 Ethrproof Intermediate Project Submission 

<b>Project Task:-</b>For this project, you will write a smart contract to create your own ERC20 token and deploy it using HardHat or Remix. Once deployed, you should be able to interact with it for your walk-through video. From your chosen tool, the contract owner should be able to mint tokens to a provided address and any user should be able to burn and transfer tokens.

## Description 

The "MyToken" contract is like creating your own special digital currency on the Ethereum blockchain. It has some basic information about the token, like its name (what it's called), symbol (a shorter code for it), how it's divided into smaller parts (decimals), and how many of these tokens exist in total (total supply). People can use this contract to send tokens to each other. It's like sending digital money to your friends. You can also say, "Hey, this person is allowed to spend my tokens up to a certain limit." It's a way to control who can use your tokens. There are some rules to make sure that only the owner can do certain things. This is to keep the money safe. The contract facilitates essential token management functionalities while adhering to the ERC20 standard.

## Code Explanation 

This is a Solidity smart contract named DegenToken that implements the ERC-20 token standard, making it suitable for creating and managing tokens on the Ethereum blockchain. The contract includes essential attributes, such as the token's name, symbol, and decimal places, which define the token's divisibility. This contract serves as a foundation for creating and managing tokens on the Ethereum blockchain, following the ERC-20 standard. It includes essential functions for transferring, approving, minting, redeeming, and burning tokens while ensuring security and avoiding common issues like overflow errors.

Token Information:

name, symbol, and decimals are public variables representing the name, symbol, and decimal places of the token.
name: "Degen Gaming Token"
symbol: "DGT"
decimals: 18 (It means you can have fractions of the token up to 18 decimal places, like dividing 1 token into 1000000000000000000 parts).
Total Supply and Balances:

_totalSupply: This is a private variable representing the total supply of tokens. It's calculated based on the initial supply provided during contract deployment.
_balances: A mapping that keeps track of the token balances for each Ethereum address.
Constructor:

The constructor sets the initial total supply and assigns it to the contract deployer's address.
It emits a Transfer event to record the initial supply.
ERC-20 Functions:

This contract implements the ERC-20 interface, which includes functions like totalSupply, balanceOf, transfer, allowance, approve, and transferFrom.
Internal Transfer Function:

_transfer: An internal function used to move tokens between addresses. It checks for valid sender and recipient addresses and ensures that the sender has a sufficient balance.
Internal Approve Function:

_approve: An internal function used to approve another address to spend tokens on your behalf.
Minting Tokens:

mint: A function that allows the contract owner (the one who deploys the contract) to create new tokens and send them to a specified address. It checks for valid recipient addresses and prevents overflow errors.
Redeeming Tokens:

redeem: A function that allows token holders to send tokens back to the contract in exchange for some action (not specified in this contract). It checks if the sender has enough tokens to redeem.
Burning Tokens:

burn: A function that allows token holders to permanently destroy some of their tokens. It checks if the sender has enough tokens to burn and if the total supply can cover the burned amount.
Access Control:

The contract inherits from the Ownable contract, which provides access control features. Only the owner (the one who deployed the contract) can mint new tokens using the mint function.

## Getting Started 

To begin programming with this type of code, the first step is to access the Solidity compiler using the Remix online Integrated Development Environment (IDE), available at: https://remix.ethereum.org/. After opening the IDE, create a new file by clicking on the "new file" option in the left-hand sidebar. Give your file a name of your choice and save it with the .sol extension, such as "first.sol." Once you have the file ready, you can proceed to write the provided code within this file.
