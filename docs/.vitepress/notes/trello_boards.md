---
name: trello-boards
description: >
  Trello boards, lists, cards CRUD and webhook REST API integration.
---

# Trello Boards CRUD Interface

## Overview
Trello uses boards, lists, and cards to organize tasks and facilitate collaboration. Its REST API allows for programmatic creation, reading, updating, and deletion of boards and card elements.

## REST API Integration
Authenticate using an API Key and Member Token:
- **Get user boards**: `GET https://api.trello.com/1/members/me/boards?key={API_KEY}&token={TOKEN}`
- **Create card**: `POST https://api.trello.com/1/cards?idList={LIST_ID}&name="Task Title"&key={API_KEY}&token={TOKEN}`
