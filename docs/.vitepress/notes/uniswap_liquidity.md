---
name: uniswap-liquidity
description: >
  Uniswap V3/V4 DeFi pools liquidity and smart contract queries.
---

# Uniswap DeFi Liquidity Interface

## Overview
Uniswap is a decentralized finance protocol that is used to exchange cryptocurrencies. The protocol facilitates automated transactions between cryptocurrency tokens on the Ethereum blockchain through the use of smart contracts.

## Core API endpoints
Programmatic integrations fetch pool reserves directly from Ethereum nodes or via subgraphs.
- **GraphQL query (The Graph)**:
  ```graphql
  {
    pools(first: 5, orderBy: volumeUSD, orderDirection: desc) {
      id
      token0 { symbol }
      token1 { symbol }
      volumeUSD
    }
  }
  ```
