# Neon EVM ERC-20-for-SPL Token Deployment Project

## Overview

This project demonstrates how to deploy a Mintable ERC-20-for-SPL token on Neon EVM and test cross-chain composability between Ethereum and Solana. The implementation uses Neon's pre-deployed Factory Contract to create a hybrid token that combines ERC-20 functionality with Solana Program Library (SPL) tokens.

## Key Components

1. **ERC-20-for-SPL Mintable Token**: A new SPL token wrapped with an ERC-20 interface
2. **TestDevBootcamp Contract**: Helper contract for testing EVM-to-Solana composability
3. **Neon EVM**: Ethereum-compatible execution environment on Solana

## Deployment Results

Here are the key addresses and transactions from the successful deployment:

### Token Contract

- **ERC20ForSPLMintable Address**: [`0xF1fd1730472288754eaF022491f89b8E879C476D`](https://neon-devnet.blockscout.com/address/0xF1fd1730472288754eaF022491f89b8E879C476D)
- **Token Mint Transaction**: [`0x413e30683962f0a995b0005c9b738bb700552b9202369bb05c303a9dd4628637`](https://neon-devnet.blockscout.com/tx/0x413e30683962f0a995b0005c9b738bb700552b9202369bb05c303a9dd4628637)

### Test Contract

- **TestDevBootcamp Address**: [`0x6A98c37b0C70b2084B14B6CA6cd82eFacD42Ae2e`](https://neon-devnet.blockscout.com/address/0x6A98c37b0C70b2084B14B6CA6cd82eFacD42Ae2e)
- **Contract Public Key**: `83n6SoortUtch4VpKGfGJMJdtFakc9EPywRmU1r4HvtM`

### Associated Token Accounts (ATAs)

- **Sender ATA**: `CcxoweVB3hkBJRVHA8yNUd8ZqCFtDnASBoJuCqJU6WU4`
- **Recipient ATA**: `4mTAddQwSJGuMDd3cB6EY1t5nNVKqjQ1rGd3FwYo1X9N`

### Transactions

1. **Approval TX**: [`0xb55af568836ca91413351b7f77f44b135813239a6e12a4dd1c37110635094612`](https://neon-devnet.blockscout.com/tx/0xb55af568836ca91413351b7f77f44b135813239a6e12a4dd1c37110635094612)
2. **Transfer TX**: [`0x08e8f5fe29b7b236ee4f424752ac21e3968f88cda456bd136ce7ab8b506557de`](https://neon-devnet.blockscout.com/tx/0x08e8f5fe29b7b236ee4f424752ac21e3968f88cda456bd136ce7ab8b506557de)

## Setup Instructions

### Prerequisites

- Node.js (v16.x or later)
- npm
- MetaMask configured for Neon Devnet

### Installation

1. Clone the repository
2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables in `.env`:

   ```env
   PRIVATE_KEY_OWNER=metamask_private_key
   PRIVATE_KEY_SOLANA=solana_private_key_in_base58
   ```

### Deployment

Run the deployment script:

```bash
npx hardhat run scripts/TestCallSolana/TestDevBootcamp.js --network neondevnet
```

## Key Features Demonstrated

1. **ERC-20-for-SPL Token Creation**
   - Using Neon's Factory Contract to mint new SPL tokens with ERC-20 interfaces
   - Mint authority assigned to your EVM wallet

2. **Cross-Chain Composability**
   - Creating Solana Associated Token Accounts (ATAs) from Solidity
   - Transferring tokens between EVM and Solana environments
   - Using Neon's precompiles for Solana interactions

## Resources

- [Neon EVM Documentation](https://docs.neonfoundation.io/)
- [Solana Devnet Explorer](https://explorer.solana.com/?cluster=devnet)
- [Neon Devnet Explorer](https://neon-devnet.blockscout.com/)
- [Neon Faucet](https://neonfaucet.org)
- [Solana Faucet](https://faucet.solana.com)
