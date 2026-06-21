# CompassMem — BCH Mempool Monitor

> Part of the [CashCompass](https://cashcompass.space) suite

Live Bitcoin Cash mempool visualizer. See what's happening inside the BCH network right now — pending transactions, fee rates, recent blocks, and network health. No API key. No build step. Pure HTML.

## Features

- **Live ticker tape** — mempool txs scroll across the top in real time
- **Mempool stats** — pending tx count, mempool size, average fee rate, best block height
- **Fee recommendation** — fast / standard / economy tiers (spoiler: BCH is always ~1 sat/byte)
- **Fee distribution chart** — pure CSS bars showing sat/byte spread across sampled txs
- **Recent blocks strip** — last 6 blocks with size, tx count, and fill percentage
- **TX feed** — live list of pending transactions with hash, BCH amount, fee rate, size
- **Network health** — avg block time, avg block size, avg txs/block

## Stack

| Layer | Choice |
|---|---|
| Data | [Haskoin Store API](https://api.haskoin.com) — CORS-open, no key required |
| Frontend | Pure HTML + CSS + vanilla JS, zero dependencies |
| Hosting | Vercel (static) |
| Repo | GitHub |

## Deploy

### 1. Fork / clone

```bash
git clone https://github.com/YOUR_USERNAME/compassmem.git
cd compassmem
```

### 2. Push to GitHub

Just push the two files — `index.html` and `vercel.json`.

### 3. Import to Vercel

1. Go to [vercel.com](https://vercel.com) → **New Project**
2. Import your GitHub repo
3. Framework preset: **Other** (no build step needed)
4. Click **Deploy**

Done. Vercel serves `index.html` as a static site. No environment variables, no serverless functions needed — Haskoin is CORS-open.

## Files

```
compassmem/
├── index.html      # The entire app
├── vercel.json     # Vercel static config + security headers
└── README.md
```

## Data refresh

The app polls Haskoin every **30 seconds** automatically. No user action required.

## Donate (BCH)

If CompassMem is useful to you, consider supporting:

`bitcoincash:qrtv37u522gz8a5lezfqk5vukly93cu7gc8tn09040`

---

Built by [@alberdioni8406_](https://x.com/alberdioni8406_) · Mozambique 🇲🇿
