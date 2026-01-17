# 🔐 Sealed-Bid Auction with Blocklock Encryption

> *Fair auctions on transparent blockchains—where cryptography, not trust, guarantees privacy.*

---

## 🎯 The Problem We Solve

Traditional blockchains are transparent by design. Every transaction is visible to everyone, instantly. This transparency is usually a feature—it builds trust. But for **sealed-bid auctions**, it's a fatal flaw.

**The Issue:**
- ❌ Early bids are visible immediately
- ❌ Later bidders can see what others offered and react accordingly  
- ❌ The fundamental principle of sealed-bid auctions—secrecy until the auction ends—is broken

This breaks fairness and opens the door to gaming the system.

---

## 💡 How We Fixed It

Instead of hoping participants follow rules or trusting a middleman, we use **Blocklock time-lock encryption**—a cryptographic innovation that makes early decryption **mathematically impossible**.

**The Magic:**
The decryption key doesn't exist until a specific blockchain block is mined. You can encrypt bids today, but no one—not even the creators—can decrypt them until the designated block height arrives. It's pure mathematics, no trust required.

---

## ⚙️ How It Works

### The Flow

```
1. 📝 Bidder submits a sealed bid (encrypted with Blocklock)
   ↓
2. 💾 Encrypted bid is stored on-chain
   ↓
3. ⏰ Time passes... blockchain keeps mining blocks
   ↓
4. 🔓 At the target block, cryptographic unlock happens automatically
   ↓
5. 🏆 Winner is determined—fairly and transparently
```

### Key Features

✨ **Encrypted Bids:** Bids remain sealed until the auction deadline  
⏱️ **Time-Lock Cryptography:** No early decryption possible—it's cryptographically enforced  
📊 **On-Chain Transparency:** Once revealed, anyone can verify the results  
🤝 **Trustless Design:** No centralized authority needed  
⚡ **Automated Execution:** Smart contracts handle everything, no manual intervention  

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v16+)
- npm or yarn
- Basic understanding of Hardhat and Solidity

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd "Sealed Bid Auction"

# Install dependencies
npm install
```

### Setup Environment

Create a `.env` file in the project root:

```env
PRIVATE_KEY=your_wallet_private_key_here
RPC_URL=your_rpc_endpoint_here
```

---

## 📋 Using the Project

### Deploy the Auction Contract

```bash
npx hardhat run scripts/deploy.js --network baseSepolia
```

### Create an Auction

```bash
npx hardhat run scripts/createAuction.js --network baseSepolia
```

### Submit an Encrypted Bid

```bash
npx hardhat run scripts/submitBid.js --network baseSepolia
```

### Request Decryption

```bash
npx hardhat run scripts/requestDecryption.js --network baseSepolia
```

### Check the Winner

```bash
npx hardhat run scripts/checkWinner.js --network baseSepolia
```

---

## 📚 Key Learnings

### Transparency is Contextual
What makes blockchains trustworthy (transparency) can break specific applications. Sometimes you need to control *when* information becomes visible.

### Math Enforces Fairness
Instead of relying on rules or intermediaries, cryptography guarantees fair outcomes. The decryption key's non-existence until a specific block is mined is enforced by mathematics, not governance.

### Timing Matters in Cryptography
Time-lock encryption flips the script. Instead of keeping secrets hidden, it keeps cryptographic keys locked behind time. Once the time passes, unlock is inevitable and verifiable.

### Threshold Networks Enable New Primitives
Blocklock uses threshold cryptography—no single entity controls the decryption key. It's distributed, decentralized, and trustless.

---

## 🌟 What's Next?

This is just the beginning. Blocklock and similar techniques unlock possibilities beyond auctions:

- **Multi-round Auctions:** Run sequential sealed-bid auctions automatically
- **Governance with Privacy:** Private voting followed by transparent results
- **NFT Marketplaces:** Sealed-bid bidding for digital collectibles
- **Time-Locked Messages:** Send messages that unlock at specific times
- **Prediction Markets:** Stake predictions without revealing them immediately
- **Game Mechanics:** Delayed reveals for fair on-chain games

---

**Built with ❤️ for a fairer blockchain.**
