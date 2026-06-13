# 🍄 ShroomLog

A private, offline **grow log for home mushroom cultivators**. Track every grow from inoculation to final flush — colonization %, pinning, harvests (flush number + yield in grams) and contamination — all in a single self-contained `index.html`.

**Live:** https://alexeysamosadov.github.io/shroomlog/

- 100% client-side, data stored in your browser's `localStorage`
- No account, no cloud, no tracking — works fully offline
- Earthy dark theme, mobile-friendly (add to home screen)

## Free vs Pro

**Free, forever:** unlimited grows, dated stage logging, per-grow timeline, days-since, total yield in grams, full history.

**Pro — one-time 9 USDC (Base):** CSV export, yield statistics per species, contamination log & clean-rate analysis, grow comparison.

## How Pro works

Pro is unlocked by a signed license key (ECDSA P-256). Pay 9 USDC on Base to the wallet shown in the app, then open a license request issue with your transaction hash. A GitHub Action verifies the on-chain payment and replies with your key automatically. Paste the key into **Pro → Have a key? → Activate**. The key is verified locally and works offline forever.

The license **private** signing key is never committed (see `.gitignore`); only the public key is embedded in the app.

## Pages

- `index.html` — the app
- `mushroom-grow-log-app.html`, `mushroom-cultivation-tracker.html` — landing pages
- `scripts/fulfill-action.mjs` + `.github/workflows/fulfill.yml` — automated license issuer
