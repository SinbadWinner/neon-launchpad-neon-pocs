#  MemeCoin Launchpad on Solana via Neon EVM

This project was developed as part of **Neon Dev Bootcamp – Week 2**.

## 📌 Overview

A fully onchain memecoin launchpad powered by **Neon EVM** and **Raydium DEX**, featuring:

- Bonding curve-based token sales
- Liquidity pool creation on Raydium
- NFT representing the locked LP position
- Composability from Solidity to Solana using Neon precompiles

## Implemented Features

 Deployment of `BondingCurve` and `MemeLaunchpad` contracts  
 Token sale initialized and configured  
 Token purchases (including reaching the funding goal)  
 Liquidity pool created on Raydium  
 LP NFT minted and fees collected via `collectPoolFees()`

##  Custom Logic

🛠 Added custom version: `MemeLaunchPadV2.sol`  
> **Changes:** 
*This version introduces a modified token sale logic in MemeLaunchpadV2.sol that replaces the traditional flat fee (e.g. 10%) with a dynamic token allocation model. Instead of deducting a percentage from user contribution, we now adjust the bonding curve parameters to indirectly include the protocol's fee in the token pricing itself.

✅ Key changes:
No direct WSOL fee deduction from user contribution.

Token price is slightly higher due to modified bonding curve configuration.

More transparent and fair token distribution — what the user pays, they fully contribute.

Protocol revenue is now earned through pricing mechanics rather than explicit cuts.

This method improves user perception and aligns incentives by avoiding hidden fees.

This version is included in the repo alongside the default contracts for bonus evaluation.

##  Getting Started

```bash
git clone https://github.com/SinbadWinner/neon-launchpad-neon-pocs.git
cd neon-launchpad-neon-pocs
npm install
cp .env.example .env
# Insert your private keys into the .env file
npx hardhat test test/MemeLaunchpad/MemeLaunchpad.js --network neondevnet

Screenshot 
![image](https://github.com/user-attachments/assets/7b8d4fad-a82d-4d49-b4d8-bc8c549ee97e)


