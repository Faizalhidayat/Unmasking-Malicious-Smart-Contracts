# 🚀 Ethereum Smart Contract Exploration: Unmasking Malicious Contracts 🚀

Welcome to the Ethereum Smart Contract Odyssey! Our mission is to identify contracts that appear genuine but are actually malicious. Here's a quick rundown of our contract constellation:

## 🌟 Contracts

1. **Good.sol**: This contract collaborates with a `Helper` to verify and manage user eligibility. It's our standard for comparison.
2. **Helper.sol**: This contract aids the `Good` contract by handling user eligibility. It's our trusted ally.
3. **Malicious.sol**: This contract pretends to be the `Helper`, but it only considers the owner as eligible. It's our main adversary.

## 🛠️ Test

To execute the test, you can use the following command:

```bash
npx hardhat test
```

This command will run the test suite using the Hardhat Ethereum development environment. Remember to ensure that all your contract files and test files are in the correct directories as specified in your Hardhat configuration.

## 🔒 Security

Remember, navigating the cosmos of smart contracts requires a keen eye for security. Always adhere to the best practices. It's our shield against potential threats.

## 📜 License

This project is licensed under the MIT License. It's our assurance of open collaboration.

Enjoy your journey and stay vigilant out there! 🚀
