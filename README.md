# Simple Flash Loan

## Overview
This smart contract demonstrates the use of Aave's **Flash Loan** mechanism. It allows a user to borrow assets without collateral, execute an operation, and repay the loan within the same transaction.

## Features
- Utilizes Aave V3's **flashLoanSimple** function.
- Demonstrates borrowing, executing an operation, and repaying the loan.
- Implements necessary approvals for loan repayment.

## Prerequisites
Before deploying or interacting with this contract, ensure you have:
- **Node.js** and **npm/yarn** installed.
- A wallet like MetaMask connected to the **Sepolia testnet**.
- **Remix IDE** or **Hardhat** for smart contract development.
- Some test ETH in your wallet for gas fees.

## Installation & Setup
Clone the repository and install dependencies:
```sh
git clone https://github.com/Vimal-Dubey/flash-loans-demo.git
cd simple-flashloan
npm install
```

## Deployment
### Using Remix IDE
1. Open **Remix IDE** and create a new file.
2. Copy-paste the `SimpleFlashLoan.sol` contract.
3. Compile the contract.
4. Deploy it using the Aave **Pool Address Provider** as a constructor parameter.

### Using Hardhat
1. Set up a Hardhat project:
   ```sh
   npx hardhat
   ```
2. Compile the contract:
   ```sh
   npx hardhat compile
   ```
3. Deploy using a script:
   ```sh
   npx hardhat run scripts/deploy.js --network sepolia
   ```

## Usage
### Request a Flash Loan
Call the function in your deployed contract:
```sh
await contract.fn_RequestFlashLoan("<TOKEN_ADDRESS>", <AMOUNT>);
```

### Implement Your Logic
Modify the `executeOperation` function to perform arbitrage, liquidation, or other DeFi strategies.

## Example Transaction Flow
1. **Check Initial Balance** 🏦
2. **Execute Flash Loan** ⚡
3. **Perform Arbitrage / Other Operations** 🔄
4. **Repay Loan + Fee** 💰
5. **Check Final Balance** 📊

## References
- [Aave V3 Flash Loans Docs](https://docs.aave.com/developers/guides/flash-loans)
- [Solidity Documentation](https://soliditylang.org/docs/)
- [Remix IDE](https://remix.ethereum.org/)

## License
This project is licensed under the **MIT License**. Feel free to fork, modify, and use it in your projects!

---
**Author:** Your Name  
**GitHub:** [your-username](https://github.com/your-username)

