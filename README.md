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

## License

MIT License.
