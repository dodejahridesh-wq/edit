---
name: alpaca-trading
description: >
  Commission-free stock and crypto trading API brokerage.
---

# Alpaca Algorithmic Trading API

## Overview
Alpaca is a commission-free API-first brokerage that enables developers to build trading algorithms, integrate investing capabilities, and build custom financial applications.

## REST API Endpoints
Alpaca uses specific endpoints for paper trading vs. live accounts.
- **Paper trading base**: `https://paper-api.alpaca.markets`
- **Submit order**: `POST /v1/orders`
  ```json
  {
    "symbol": "AAPL",
    "qty": 1,
    "side": "buy",
    "type": "market",
    "time_in_force": "day"
  }
  ```
- **List positions**: `GET /v1/positions`
