# SpectrumMint 🚀

A high-performance Solana memecoin launchpad and trading dashboard with real-time bonding curve integration, TradingView-style candlestick charting, and automatic DexScreener synchronization.

## Features

- **Instant Bonding Curve Token Deployment**: Deploy tokens to Solana mainnet via Pump.fun / PumpPortal.
- **Custom Token Metadata**: Auto-pinning of token logos and metadata JSON to IPFS via Pinata.
- **Authority Revocations**: Support for revoking Freeze, Mint, and Metadata Update authorities.
- **TradingView-Style Candlestick Chart**: Real-time candlestick charts with proportional wicks, live price crosshair, and customizable views (Market Cap & SOL Price).
- **Live Trade Ledger**: Streamlined, real-time ledger tracking bonding curve swaps and transactions.
- **Dev Allocation Management**: Transparent holding and on-chain liquidation options directly from the creator dashboard.
- **Multi-Wallet Support**: Seamless Phantom and Solflare wallet adapter integrations with live on-chain balance updates.

## Tech Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES Modules)
- **Bundler**: Vite
- **Solana Web3**: `@solana/web3.js`, `@solana/spl-token`, `tweetnacl`
- **APIs**: PumpPortal Local Trade API, DexScreener API, Pinata IPFS API

## Environment Variables for Vercel

When deploying to **Vercel**, add the following environment variable in **Project Settings → Environment Variables**:

| Variable Name | Required | Default / Value | Description |
| :--- | :--- | :--- | :--- |
| `VITE_PINATA_JWT` | **Yes** | `eyJhbGci...` | Pinata IPFS JWT token used to pin token images and metadata JSON. |
| `VITE_SOLANA_RPC_URL` | No | `https://solana-rpc.publicnode.com` | Optional custom Solana Mainnet RPC endpoint (e.g. Helius / QuickNode). |

### Note on APIs:
- **PumpPortal Local Trade API (`https://pumpportal.fun/api/trade-local`)**: Does **not** require an API key. It is a public local transaction creation endpoint signed locally by the user's wallet.
- **DexScreener API (`https://api.dexscreener.com`)**: Does **not** require an API key. It is a completely free, open public REST API.
- **Pinata IPFS API**: Requires the `VITE_PINATA_JWT` key above for uploading images and metadata.

## Getting Started

### Prerequisites

- Node.js (v18+)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/EdTech20/SpectrumMint.git
cd SpectrumMint

# Install dependencies
npm install

# Run the local development server
npm run dev
```

### Production Build

```bash
npm run build
npm run preview
```

## Vercel Deployment

1. Import your GitHub repository (`EdTech20/SpectrumMint`) into **Vercel**.
2. Framework Preset: **Vite** (detected automatically).
3. Add the `VITE_PINATA_JWT` Environment Variable.
4. Click **Deploy**!

## License

MIT License.

