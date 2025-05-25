Here's a `README.md` file with all the transaction logs and essential notes from your Hardhat test run, neatly formatted for documentation:
# 🚀 Godspower MemeLaunchpad Deploy

Welcome to **Godspower MemeLaunchpad** — a fully on-chain memecoin launchpad built on **Neon EVM**, seamlessly integrated with **Solana**.

With this platform, anyone can:
- 🚀 Launch a token sale
- 💰 Raise SOL
- 🔐 Instantly lock liquidity on **Raydium DEX**

...all powered by smart contracts.

---

### 🧠 Why It’s Special

Memecoins go **brrr**, but this time they’re running on **Solana** — using **Solidity**! 😎  
Enjoy the speed and low fees of Solana, while building with EVM-compatible tools you already know.

---

### 🌐 Tech Stack

- **Solidity**
- **Neon EVM** (EVM on Solana)
- **Raydium** (for liquidity)
- **Hardhat** for development and testing

---

### 📌 Features

- Create and manage onchain token sales
- Automatically handle SOL contributions
- Lock LP tokens to Raydium via NFT-based vaults
- Fee collection and claim logic
- Gas-efficient bonding curve

---

Let the memes flow — transparently, permissionlessly, and on-chain.

---

```markdown
# MemeLaunchpad Smart Contract Test Logs

This document contains logs of transaction outputs and test status for the `MemeLaunchpad` contract tested on the `neondevnet` network.

---

## 🧪 Test Suite: `test/MemeLaunchpad/MemeLaunchpad.js`

### Network: `neondevnet`

### ✅ BondingCurve Contract Deployed At:
```

0x0Fc6Ec7F9F06bd733913C1Fcd10BFc959a1F88DC

```

---

## ⚙️ MemeLaunchpad Contract Deployment

### ✅ MemeLaunchpad Deployed At:
```

0x01D16927d2968ff1b52B6779177beCA56c12F66c

```

---

## 🧪 Test Cases & Transaction Logs

### ✔ `createTokenSale`
**Tx Hash:**
```

0x859dbd1c986e36b689b5f9d1a6420143449bd5606998c980f6ac9c0b163e6742

```

**Info:**
- Creating ATA accounts for the following SPL Tokens:
  - `So11111111111111111111111111111111111111112`
  - `6NJR5gcGP15ZFeSQUupckRAiWw2pJaYPj5fZAZKT9uXV`

**Tx Signature:**
```

osCbpKKBPMGoWK35vBoZu9bWcMwMiiS886ZMzFHDijnofdcgx6LwhxzF2gP4ATFwLVtce6yjzcd4q7pX9SLseAb

```

---

### ✔ `buy (not reaching the fundingGoal)`
**Tx Hash:**
```

0xa243cd718cfa3ac26744ffa129954d2c77d8f1e187732c7b15baa7243141039f

```

---

### ❌ `buy (reaching the fundingGoal)`
**Tx Hash:**
```

0x6a90afe1033fdc30f93e4dcf8d88d43f4780b50733956acc159f85258ddf33ba

```

**Raydium Pool ID Account:**
```

F7tvUa55uR6Jj2nEa9LSFQ4pR1BRFMXqK9s9P4zrQ612

```

**Locked LP Amount:**
```

14142135523

```

**NFT Account Holding Locked LP:**
```

ANnSNRdX2RRVq1NWyTxpdgXF3qEbNS2HfF9oGHHqMXud

```

---

### ✔ `claimTokenSaleFee`
**Tx Hash:**
```

0x7ee69fd0cc0449b1f125a80813292ece52cd140cc797f8780b75b076b7d16b38

```

**Simulated Raydium Swap Input:**
```

F7tvUa55uR6Jj2nEa9LSFQ4pR1BRFMXqK9s9P4zrQ612

```



---

### ✔ `collectPoolFees`
**Tx Hash:**
```

0x86df88e191438ac5be07a472da0124bd49737a340645859f042090ae291d8344

```

**Tx ID:**
```

2RzmxMgQ6vS1wQbv3D4f3Mta6hATKraXHGndCtaQ9G2NMwKUJtz4egbKUQjbCrHqxnySJx6EoKZRRVrdHaJNnRVQ

````

---
