## Unmasking Malicious Smart Contracts 

Welcome to our Ethereum Smart Contract Ecosystem! This is a collection of smart contracts developed using Solidity, a statically-typed programming language designed for the Ethereum blockchain. Our theme is identifying genuine-looking contracts which are actually malicious. Let's unmask them!

## 📖 Contracts

### 🏆 Good Contract

The `Good` contract is our protagonist. It interacts with a sidekick contract known as `Helper`. It has two main functions: `isUserEligible` and `addUserToList`. The `isUserEligible` function checks if a user (address that calls this function) is eligible by calling the `isUserEligible` function of the `Helper` contract. The `addUserToList` function adds a user to a list by calling the `setUserEligible` function of the `Helper` contract.

### 🛠️ Helper Contract

The `Helper` contract is the trusty sidekick. It maintains a mapping called `userEligible` that maps addresses to boolean values. It has two functions: `isUserEligible` and `setUserEligible`. The `isUserEligible` function accepts an address as a parameter and returns a boolean indicating whether the user associated with the address is eligible or not. The `setUserEligible` function accepts an address as a parameter and sets the corresponding value in the `userEligible` mapping to `true`, indicating that the user is eligible.

### 🕶️ Malicious Contract

The `Malicious` contract is the villain in disguise. It's similar to the `Helper` contract, but the `isUserEligible` function has been modified to return `true` only if the user is the owner of the contract. This could be a potential security risk if the intention is to check eligibility for all users, not just the owner. This contract serves as a reminder that not all contracts are as they appear, and we must always be vigilant.

## 🧪 Test

We have a test script that deploys the `Malicious` and `Good` contracts, gets an address from the list of available signers, calls the `addUserToList` function of the `Good` contract with the address, calls the `isUserEligible` function of the `Good` contract with the same address, and checks if the returned value is `false`. This test helps us unmask the malicious behavior of the `Malicious` contract.

## 🔐 Security

Please note that this contract system could be potentially malicious or have unintended behavior due to the modification in the `isUserEligible` function of the `Malicious` contract. Always ensure to follow best practices for security and efficiency when writing and deploying your smart contracts. Solidity is a powerful language, but with it comes the responsibility of ensuring your code is safe and efficient.

## 📄 License

This project is licensed under the MIT License.

Enjoy exploring our Ethereum Smart Contract Ecosystem and remember, stay vigilant! 🚀
 
