# 🧪 Week 2 Submission – Memecoin Launchpad on Solana Using Neon EVM

This week, I built a fully onchain **Memecoin Launchpad** using Solidity on **Neon EVM**, connected to Solana.
The launchpad lets anyone run a public token sale, with tokens sold via a bonding curve and liquidity locked on **Raydium DEX**.

---

## ⚙️ Setup I Used

### Environment

* **Neon EVM (Devnet)**
* **Solana (Devnet)**
* **Hardhat** for deployment and tests
* **Node.js** and **npm**

### Steps

1. Cloned the base repo:
   `git clone git@github.com:neonlabsorg/neon-pocs.git`

2. Installed packages:
   `npm install`

3. Set up `.env` using `.env.example`:

```env
PRIVATE_KEY_OWNER=evm-wallet-private-key
PRIVATE_KEY_SOLANA=solana-wallet-private-key
USER1_KEY=random-32-byte-key
```

4. Got test tokens from:

* [https://neonfaucet.org](https://neonfaucet.org)
* [https://faucet.solana.com](https://faucet.solana.com)

---

## 🧪 Test Run Output

Here’s what happened when I ran:

```bash
npx hardhat test test/MemeLaunchpad/MemeLaunchpad.js --network neondevnet
```

* `BondingCurve` deployed at:
  `0x0Fc6Ec7F9F06bd733913C1Fcd10BFc959a1F88DC`

* `MemeLaunchpad` deployed at:
  `0x519Bf10a916cC2096c1355D73B53e5CCADcDBf0B`

* `createTokenSale txn` deployed at:
  `0x792c31bcfa03c6aab6f82067250edfcfd9dd6684aa10bd5c30d6a5fa9c0c1b43`

* `createTokenSale txn signature` deployed at:
  `MAzhNwzcyURB53mypgmFNutYkuZs5sARaKbZxKZjRQaMEELyyt9PjL3UXBf8znjRUGcBxXnCqtwBVBYLsnWtcFF`

* `claimTokenSaleFee txn` deployed at:
  `0x91377485736d278787bd926d569cb6a92d36f05a4cb083049f33b7d6ea826b2d`

### Sale Lifecycle Steps

1. **Token Sale Created**

   * Used bonding curve
   * Set funding goal to 0.1 SOL
   * ATA accounts created for:
     `So11111111111111111111111111111111111111112` and `6dPwA9WEfoxCdrW59HFemo2uJhQd1fwSqAdittXV9pzb`

2. **First Buy**

   * Sent 0.01 SOL
   * Below goal, sale still active

3. **Second Buy**

   * Sent 0.15 SOL
   * Goal reached
   * Triggered pool creation

4. **Liquidity Locked**

   * Raydium CPMM pool created
   * NFT minted to represent LP lock

5. **Fee Collection**

   * Simulated pool swaps
   * Collected fees via `collectPoolFees()`

---

## 🔍 What I Learned

* How to build bonding curve logic in Solidity
* How to use precompiled contracts like `ICallSolana`
* How EVM can call Solana programs like Raydium
* How to handle WSOL deposits and ATA creation
* How Neon abstracts Solana complexities into Solidity calls

---

## 📁 Contracts I Worked With

* `/contracts/BondingCurve.sol`
* `/contracts/MemeLaunchpad.sol`

## 📄 Test Script

* `/test/MemeLaunchpad/MemeLaunchpad.js`

---

## 🏁 Task Completed

✅ Built and tested the Memecoin Launchpad
✅ Connected EVM contracts to Solana programs
✅ Created and locked liquidity on Raydium
✅ Used composability features from Neon EVM
✅ Collected fees through pool trading activity
