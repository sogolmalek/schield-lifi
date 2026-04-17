# ⛨ Shield — Rug Score + Safe Swap Everywhere

> See a token. See its score. Buy it safe from any chain.

**Shield** is a Chrome extension that overlays real-time rug pull risk scores on every Solana token — and lets you **buy safe via cross-chain swap** powered by [LI.FI](https://li.fi).

## Architecture

```
Token on Twitter → Shield scores it → 🟢 78 "Buy Safe via LI.FI"
                                     → 🔴 14 🛑 BLOCKED

Click "Buy Safe" → LI.FI routes best path across 20+ bridges → Token in your wallet
```

## LI.FI Integration (Core)

LI.FI is the **execution layer**. Every swap routes through LI.FI:
- Cross-chain swaps: ETH on Ethereum → Solana token in one click
- DEX aggregation: Jupiter, DFlow, Titan, OKX, Fly
- Bridge aggregation: 20+ bridges × 60+ chains  
- Shield + LI.FI = first cross-chain swap that **blocks rug pulls**

## Security: 8 checks via RugCheck + Alchemy RPC

Mint Authority · Freeze Authority · LP Lock · Top Holder % · Dev Wallet % · Honeypot · Liquidity · Token Age

## Revenue

- $0.01 USDC/scan via x402 on Solana
- Free tier: 10 scans/day × 3 days
- Swaps route through LI.FI (default commission)
- Wallet: `A59AVvijPfVC62vxpWqHevgc5FEaQ6bEEmdvSdMYDebs`

## Stack

Chrome Extension (Manifest V3) · RugCheck API · Alchemy RPC · **LI.FI** (swaps) · x402 (payments) · Solana

## Deploy

```bash
cd backend && npm install && node server.js   # Backend
# Update SHIELD_API in extension/src/content.js
# chrome://extensions → Load Unpacked → extension/
```

## Links
- Demo: https://shieldme.netlify.app
- Solana Frontier Hackathon × LI.FI Track

MIT License
