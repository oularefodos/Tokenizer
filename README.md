# Game42 Token – ERC20-Compatible Token on BNB Chain

## 🧩 Project Overview

**Game42 (G42)** is a BEP-20 (ERC20-compatible) token deployed on BNB Smart Chain. Developed as part of the "Tokenizer" project from 42 School in partnership with BNB Chain, this token is designed to showcase ownership control, minting, burning, transfers, and allowances.

## 🛠 Stack

- **Blockchain:** BNB Smart Chain (Testnet)
- **Language:** Solidity ^0.8.28
- **Framework:** Hardhat
- **Token Standard:** BEP-20 (ERC20 compatible)

## 📦 Folder Structure

├── README.md
├── code # Contains the token smart contract
│ └── GameToken.sol
├── deployment # Contains deployment scripts and Hardhat configs
│ ├── deploy.js
│ └── hardhat.config.js
└── documentation # Contains functional and usage documentation
└── overview.md

## 🎮 Token Details

- **Name:** Game42
- **Symbol:** G42
- **Decimals:** 18
- **Initial Supply:** 42 G42 (minted to deployer)

## ✍️ Contract Features

- ✅ Ownership control via `Ownable`
- ✅ `transfer`, `approve`, `transferFrom` fully compliant with ERC20
- ✅ `mint` and `burn` functions restricted to owner
- ✅ Allowance increase/decrease helpers
- ✅ Events emitted for all major operations

## ⚙️ Setup and Deployment

### 1. Clone & Install

```bash
git clone <repo_url>
cd <repo_name>
npm install

## Compile Contracts
```bash
npx hardhat compile
npx hardhat run --network testnet deployment/deploy.js
 