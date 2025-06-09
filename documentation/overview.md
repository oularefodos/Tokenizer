
# Game42 Token Documentation

## Summary

Game42 (G42) is a BEP-20 token implementation designed to teach tokenomics, smart contract development, and security using Solidity and Hardhat on the BNB Chain Testnet.

The token has:

- A fixed initial supply of **42 tokens**, where **1 G42 = 10¹⁸ units** (standard 18 decimals).
- Entire supply minted to the deployer's address upon contract creation.


## Features

### 1. Ownership Management

- Only the contract deployer is granted `onlyOwner` permissions.
- Ownership can be transferred using `transferOwnership(address newOwner)`.

### 2. ERC20 Core Functions

| Function          | Description                        |
|------------------|------------------------------------|
| `totalSupply()`  | Returns total token supply         |
| `balanceOf()`    | Returns balance of a given address |
| `transfer()`     | Transfers tokens to another address|
| `approve()`      | Approves spender for allowance     |
| `transferFrom()` | Transfers on behalf of holder      |
| `allowance()`    | Shows allowance value              |

### 3. Custom Extensions

#### `mint(uint256 amount)`
- Only accessible by the owner
- Mints `amount` tokens to the owner address

#### `burn(uint256 amount)`
- Only accessible by the owner
- Burns `amount` tokens from the owner’s balance

#### `increaseAllowance` / `decreaseAllowance`
- Safe management of token approvals

### Requirements

- Node.js
- Hardhat
- `.env` file with `PRIVATE_KEY` and `RPC_URL`

## 🔁 Usage Examples (with Hardhat console or scripts)

Make sure to import `ethers` from Hardhat to handle token units correctly:

### Exemple
```js
const { ethers } = require("hardhat");
const amount = ethers.utils.parseUnits("5", 18); // 5 G42 tokens
await token.transferFrom("0xYourAddress", "0xRecipientAddress", amount);


### Example `.env`
PRIVATE_KEY=your_private_key
RPC_URL=https://data-seed-prebsc-1-s1.binance.org:8545/
