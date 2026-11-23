# ⚡ CryptoRave Mining

Neon cyber SPA that simulates BTC mining, subscription plans, weekly competitions, and horse racing.

**Live features (frontend)**
- Mining console with hashrate / temp / power visualisation
- 4 plan tiers (Starter → Whale)
- Global competition leaderboard + prize pool
- Crypto Derby horse racing with betting UI
- Wallet, deposits, withdrawals, auth modals

> All balances, rewards and race outcomes are expected from a backend at `/api/*`. Without a server the UI still works as a full visual demo.

## Quick deploy (Vercel)

1. Replace `index.html` with the full source from the Grok artifact (`CryptoRave_Mining.html` renamed to `index.html`).
2. Import this repo at [vercel.com/new](https://vercel.com/new).
3. Framework Preset: **Other** (or leave blank).
4. Deploy.

Your site will be live at `https://cryptorave-mining.vercel.app` (or the name you choose).

## Local preview

```bash
npx serve .
# or
python3 -m http.server 3000
```

Open http://localhost:3000

## Stack

- Single-file HTML + CSS + vanilla JS
- Google Fonts: Orbitron, Share Tech Mono, Rajdhani
- Neon cyber palette (`#ff0080` → `#aa00ff`)
- No build step required

## Backend notes

The client talks to:
- `POST /api/login` / `signup` / `logout`
- `POST /api/mining/start|stop|claim`
- `POST /api/race`
- `POST /api/create-checkout-session` (Square)
- `GET  /api/me` / `stats`
- Wallet + KYC endpoints

Point these at your own server or mock them for demos.
