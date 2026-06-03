---
name: coingecko-market
description: >
  Cryptocurrency market data feeds, indices, and DEX tickers API.
---

# CoinGecko Crypto Feed API

## Overview
CoinGecko provides fundamental analysis of the crypto market. It tracks price, volume, market capitalization, community development, and developer metrics.

## REST API Integration
CoinGecko offers public and developer REST APIs that do not require complex signatures.
- **Check service status**: `GET https://api.coingecko.com/api/v3/ping`
- **Retrieve current prices**: `GET https://api.coingecko.com/api/v3/simple/price?ids=bitcoin,ethereum&vs_currencies=usd`
- **List coins**: `GET https://api.coingecko.com/api/v3/coins/list`
