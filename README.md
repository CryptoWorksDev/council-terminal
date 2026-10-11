# Council Terminal

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-Proprietary-red.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey.svg)]()

A proprietary, multi-threaded microstructure monitor designed to detect hidden liquidity, order book spoofing, and structural market imbalances across 5 major cryptocurrency exchanges in real-time.

> **Note:** The core detection engine is a closed, proprietary system. This repository serves as an architectural overview and documentation hub.

## The Problem

Most retail trading tools rely on surface-level price and volume data. Institutional algorithms, however, operate in the gaps: hiding accumulation behind iceberg orders, manipulating sentiment with spoofed walls, and creating structural traps (like long/short squeezes). Standard screeners cannot see this microstructure.

## The Engine (Conceptual Architecture)

Council Terminal solves this by analyzing the divergence between visible order book depth and actual trade executions across Binance, Bybit, KuCoin, OKX, and Kraken simultaneously.

- **FLOW:** Tracks actual executed trade volume. Flags "Icebergs" when execution exceeds visible depth, and "Shadow Breaks" when large volume moves with zero visible support.
- **MIRAGE:** Scans the top levels of the order book for anomalous, static walls. Tracks their lifecycle to distinguish genuine liquidity from manipulation (spoofing).
- **NEXUS:** The confluence engine. Cross-references FLOW and MIRAGE data, applying deduplication tolerance and cascading API fallbacks to generate high-confidence verdicts (`CONFIRMED`, `FAKE`, `HIDDEN BUYER/SELLER`).

## Live Capture

![Council Terminal Interface](assets/terminal_screenshot.png)

*Real-time detection of structural anomalies: spoofed walls, hidden liquidity, and cross-exchange confluence signals across 5 major exchanges.*

## Resources & Live Feed

- **Live Anomaly Feed:** The terminal runs 24/7, posting curated, delayed digests of market microstructure events to our public channel: [t.me/council_terminal](https://t.me/council_terminal)

## Tech Stack

- **Language:** Python 3.9+
- **GUI:** Flet / CustomTkinter
- **Data:** ccxt, websockets, requests
- **Resilience:** Custom cascading API fallback mechanism and global exception handling for 24/7 autonomous uptime.

---

*Built for institutional-grade visibility. Signal > Noise.*
