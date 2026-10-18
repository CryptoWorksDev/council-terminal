# 🦉 Council Terminal

> *Seeing not just the price, but the intentions behind it.*

**Council Terminal** is a professional cryptocurrency market microstructure analysis tool, developed by **Crypto Works**. Unlike traditional charts that show only past prices, our terminal visualizes hidden market processes: limit walls, their absorption, and the real imbalance between buyers and sellers — in real time.![Council Terminal LEVIATHAN](assets/terminal_leviathan.png)

*Screenshot: Council Terminal v1.0.0 — LEVIATHAN tier, all modes active.*

---<img width="1916" height="1032" alt="terminal_leviathan" src="https://github.com/user-attachments/assets/f7c6b797-587e-45ff-b35c-f6e3ce0c1468" />


[![Version](https://img.shields.io/badge/version-1.0.0--prototype-blue)]()
[![Python](https://img.shields.io/badge/python-3.10+-yellow)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)]()
[![Status](https://img.shields.io/badge/status-In_Development-orange)]()

---

## 🚧 Project Status

Follow our progress in the official Telegram channel: [t.me/council_terminal](https://t.me/council_terminal)

---

##  Core Architecture

Council Terminal solves a key problem: most retail trading tools rely on surface-level price and volume data. Institutional algorithms, however, operate in the gaps — hiding accumulation behind iceberg orders, manipulating sentiment with spoofed walls, and creating structural traps (like long/short squeezes). Standard screeners cannot see this microstructure.

Our engine analyzes the **divergence between visible order book depth and actual trade executions** across 5 major exchanges simultaneously:

- **FLOW** — Tracks actual executed trade volume. Flags "Icebergs" when execution exceeds visible depth, and "Shadow Breaks" when large volume moves with zero visible support.
- **MIRAGE** — Scans the top levels of the order book for anomalous, static walls. Tracks their lifecycle to distinguish genuine liquidity from manipulation (spoofing).
- **NEXUS** — The confluence engine. Cross-references FLOW and MIRAGE data, applying deduplication tolerance and cascading API fallbacks to generate high-confidence verdicts: `CONFIRMED`, `FAKE`, `ATTACK`, `SHADOW BREAK`, `HIDDEN BUYER/SELLER`.

---

## 🔹 Key Features

- **5-tier access system:** From free `MICRO` to professional `LEVIATHAN`
- **Velocity metrics:** Real-time % change calculation for 1m, 5m, 15m, and 1h intervals
- **META panel:** Exchange stress, smart money activity anomaly detection, API instability, event throughput — with EMA smoothing and sparkline visualization
- **ORACLE AI zone:** Reserved for higher tiers — AI-powered market narrative analysis (coming soon)
- **Adaptive layout:** Automatically adjusts to screen resolution, minimum 1280×720

---

## 🗺️ Roadmap

| Phase | Milestone | Status |
|-------|-----------|--------|
| 1.0 | UI/UX prototype with mock data | ✅ Complete |
| 1.1 | ORACLE AI module (market narrative analysis) | 📋 Planned |
| 1.2 | SQLite license database + key generation | 📋 Planned |
| 2.0 | Multi-asset support (ETH, SOL, etc.) | 📋 Planned |

---

## 📥 Getting Started.

*For access to SCOUT tier and above during the beta phase, contact us via Telegram.*

---

## 🔗 Links

- 📢 **Telegram Channel (Dev Log & Alerts):** [t.me/council_terminal](https://t.me/council_terminal)
- 🎥 **YouTube Demo:** *[Coming Soon]*
- 📩 **Contact:** [cryptoworksdev@proton.me](mailto:cryptoworksdev@proton.me)

---

## ⚠️ Disclaimer

This tool is provided **"as is"** for analytical and educational purposes only. It does not constitute financial advice, investment recommendations, or a call to action. All trading decisions are made at the user's own risk. Conduct your own due diligence.

---

*© 2026 Crypto Works. All rights reserved.*
