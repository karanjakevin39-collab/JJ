# 🌐 Aggregator

**Aggregator** is a cross-chain dust collection and swapping platform designed to help users consolidate small balances ("dust") from various chains — currently supporting **Stellar**, **StarkNet**, and **Ethereum** (Ethereum support is passive for now).

This MVP allows users to connect their wallets, select token balances across chains, and seamlessly transfer and swap them into a preferred stable currency like **USDC** on **Stellar**.

---

## 🚀 Getting Started

### Prerequisites

- **Node.js 20+**
- npm
- Browser wallet extensions for the chains you want to test:
  - Stellar: Freighter or another Stellar-compatible wallet
  - StarkNet Sepolia: Argent X or Braavos
  - Ethereum Sepolia: MetaMask or another EVM wallet

Use testnet accounts only. Do not use mainnet funds while testing this MVP.

### Run Locally

```bash
npm install
npm run dev
```

If npm reports a React peer dependency conflict, install with the existing peer dependency set:

```bash
npm install --legacy-peer-deps
npm run dev
```

Open the local development URL shown in your terminal, usually `http://localhost:3000`.

### Testnet Funding

#### Stellar Testnet

1. Create or select a Stellar testnet account in your wallet.
2. Copy the public account address.
3. Open [Stellar Laboratory](https://laboratory.stellar.org/) and use Friendbot to fund the account with 10,000 testnet XLM.
4. Verify the balance in your wallet, in Stellar Laboratory, or with a Stellar testnet explorer.

#### StarkNet Sepolia

1. Switch your StarkNet wallet to Sepolia.
2. Copy your StarkNet Sepolia account address.
3. Request testnet STRK or ETH from the [StarkNet Sepolia faucet](https://starknet-faucet.vercel.app/).
4. Verify the balance in your wallet or on a StarkNet Sepolia explorer.

#### Ethereum Sepolia

1. Switch your EVM wallet to the Ethereum Sepolia network.
2. Copy your Sepolia account address.
3. Request Sepolia ETH from [Sepolia Faucet](https://sepoliafaucet.com/) or [QuickNode Sepolia Faucet](https://faucet.quicknode.com/ethereum/sepolia).
4. Verify the balance in your wallet or on an Ethereum Sepolia explorer.

After funding a test account, connect the matching wallet in the app and refresh balances to confirm the account is ready for local testing.

---

## 🚀 Features

- 🔗 **Multi-chain support**:  
  - ✅ Stellar (Active)  
  - ✅ StarkNet (Active)  
  - 🕓 Ethereum (Passive only; no logic yet)
  
- 🧠 **Smart dust collection flow**:
  - Connect your wallet
  - View and select token balances
  - Transfer selected tokens for processing
  - Swap them into **USDC** (or another Stellar currency)
  
- 💰 **Minimum Threshold**:  
  To maintain efficiency, there's a minimum required amount for processing. Tiny fractions are ignored or bundled as needed for gas optimization.

---

## 🧭 Usage Flow

1. **Connect your wallet**  
   - Click the **Connect Wallet** button to link your Stellar or StarkNet wallet.
   
2. **Select balances**  
   - Once connected, available balances are shown. You choose which tokens you want to aggregate.
   
3. **Process balances**  
   - The selected tokens are transferred and bundled for aggregation.

4. **Swap to Stellar currency**  
   - After processing, tokens can be swapped into a Stellar-based currency such as **USDC**.
   - You may choose which Stellar currency to receive.

5. **Close transaction**  
   - Once swapped, your balances are ready for withdrawal or donation.

---

## 🛠️ Tech Stack

- **Frontend**: Minimal UI with wallet connection and balance selection interface  
- **Smart Contracts**:  
  - Stellar: Handles transfers and swaps  
  - StarkNet: Used for dust balance selection and transfer  
  - Ethereum: Currently no active logic, may be supported in future updates

---

## 🧪 Status

This project is an MVP and still under development.  
Active logic is being implemented on **Stellar** and **StarkNet** only for now. Ethereum is passive — no active transfer or swap logic yet.

---

## 🧼 Coming Soon

- Full Ethereum integration  
- UI polish and responsiveness  
- Donation & withdrawal tracking  
- Analytics for token collection impact

---

## 📝 License

MIT License. Use freely and contribute if you'd like.
