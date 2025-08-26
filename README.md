# LEO_BOT — Solana Meme-Coin Alerts

> Real-time alert bot for **Solana meme coins**. It aggregates signals across major Solana platforms, applies strict quality filters, avoids likely rugs, and posts clean notifications to a **Telegram channel** only when market and filter criteria are met.

---

## Highlights
- 🔔 **Live notifications** to your Telegram channel  
- 🧠 **Quality filters**: market cap, volume, holders, pair age (time/mins), **Top-10 holders concentration**  
- 🛡️ **Rug-avoidance rules** to drop unsafe/unknown snapshots whenever possible  
- 📊 **Only posts “fit” tokens** matching the active market window and your thresholds  
- 🌐 **Covers Solana platforms** for meme-coin discovery (launchpads, DEX trackers, on-chain feeds)

---

## How it Works (brief)
1. Collects listings and on-chain snapshots from multiple Solana sources.  
2. Picks the best trading pair (liquidity & quote).  
3. Applies your **effective filters** (baseline + runtime overrides).  
4. If a token passes and market is suitable, the bot posts a concise Telegram alert.  
5. The system keeps tracking tokens for performance and growth milestones.

---

## Filters & Rules
- **MCAP**: min/max  
- **Volume**: min/max  
- **Holders**: min/max  
- **Pair Age**: textual (e.g., `10m`, `3h`) and/or minute bounds  
- **Top-10% concentration**: min/max  
- Unknown or out-of-range Top-10% → **rejected**.  
- Internal safety checks aim to **avoid rugs** (best-effort, not a guarantee).

---

## Delivery
- Channel-friendly messages with clear numbers and short context.  
- Optional branded visuals for growth milestones (PnL cards).

---

## Tech Stack
- 🦀 **Rust ~75%** — high-throughput data path & safety checks  
- 🐍 **Python ~25%** — orchestration, Telegram I/O, rendering

