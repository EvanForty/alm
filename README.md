# ALM — Launch a coin. Automate the liquidity.

Static website for ALM, the Solana launchpad where every coin opens with its own automated liquidity management agent.

Follow: https://x.com/ALMLaunch

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole site: styles, Range desk simulator, Solana wallet connect, agent launcher |
| `favicon.png` | Browser tab icon |
| `alm-logo.png` | Pipeline network logo artwork |
| `vercel.json` | Vercel config (clean URLs, security and cache headers) |

There is no build step and nothing to install. `@solana/web3.js` 1.95.3 loads from jsDelivr.

## Deploy on Vercel

1. Push these files to the root of a GitHub repo.
2. In Vercel, choose **Add New → Project** and import the repo.
3. Leave Framework Preset as **Other**, Build Command empty and Output Directory empty.
4. Click **Deploy**.

## Run locally

Wallet extensions don't connect to pages opened as files, so serve the folder:

```bash
npx serve .
```

## Configuration

- **RPC:** in `index.html`, set `RPC_URL` to a dedicated Solana RPC (Helius, Triton, QuickNode). The public endpoint is rate limited.
- **Wallets:** Phantom, Solflare and Backpack are detected automatically.
