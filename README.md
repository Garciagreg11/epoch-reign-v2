# epoch-reign-v2
“Smart contract for collector-gated minting, royalty enforcement, and lore-driven NFT drops on Base.”
# EPOCH//REIGN V2

**Smart Contract for Collector-Gated Minting, Royalty Enforcement, and Lore-Driven NFT Drops on Base**

This contract marks the ignition of the next EPOCH—an ERC-721A deployment forged for mythic continuity. It binds to the original $EPOCH token and Uniswap V4 liquidity pool, enforcing royalties, gating minting by token ownership, and unlocking lore-based collector quests.

---

## 🔗 Contract Overview

- **Standard**: ERC-721A (gas-efficient batch minting)
- **Gating**: Requires ownership of $EPOCH token  
  → Contract: `0x54E2ACaB04C89A3Fe02852BF8dd69Ee8F526bC75`
- **Royalties**: Enforced via ERC-2981 (default 5%)
- **Supply Cap**: 100 NFTs
- **Chain**: Base

---

## ⚔️ Collector Gating Logic

Only holders of $EPOCH tokens may mint:

```solidity
require(epoch.balanceOf(msg.sender) > 0, "Must hold EPOCH to mint.");
