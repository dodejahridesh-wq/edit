---
name: steam-integration
description: >
  Steam Web API integrations to query game stats and user achievements.
---

# Steam Integration Web API

## Overview
Valve provides the Steam Web API, allowing developers to query user achievements, friend lists, owned games, game statistics, and store listings.

## REST API Endpoints
The Web API is structured under `api.steampowered.com`.
- **Get user owned games**: `GET http://api.steampowered.com/IPlayerService/GetOwnedGames/v0001/?key={API_KEY}&steamid={STEAM_ID}&format=json`
- **Get achievements status**: `GET http://api.steampowered.com/ISteamUserStats/GetPlayerAchievements/v0001/?appid={APP_ID}&key={API_KEY}&steamid={STEAM_ID}`
